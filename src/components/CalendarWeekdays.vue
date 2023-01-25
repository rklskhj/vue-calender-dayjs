<template>
  <ol class="day-of-week">
    <li v-for="weekday in weekdays" :key="weekday">{{ weekday }}</li>
  </ol>
</template>
<script>
const WEEKDAYS = ["월", "화", "수", "목", "금", "토", "일"];

export default {
  name: "CalendarWeekdays",
  computed: {
    weekdays() {
      return WEEKDAYS;
    },
  },
};
</script>
<style scoped>
.day-of-week {
  display: grid;
  grid-template-columns: repeat(7, 1fr);
}

.day-of-week > * {
  text-align: right;
  padding-right: 5px;
  font-weight: bold;
}
</style>
