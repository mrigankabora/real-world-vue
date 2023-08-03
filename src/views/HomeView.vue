<script setup lang="ts">
import { ref } from 'vue';
import EventCard from '@/components/EventCard.vue';
const eventData = ref ([
  {
    id: 1,
    title: 'concert-1',
    time: '9:30 pm',
    date: '23/09/2023'
  },
   {
    id: 2,
    title: 'concert-2',
    time: '5:30 pm',
    date: '27/09/2023'
  }
])
</script>

<template>
  <div class="events">
    <EventCard v-for="event in eventData" :key='event.id' :event=event />
  </div>
</template>
<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>