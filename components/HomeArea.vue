<template>
  <div>
    <Line class="charts" :data="temperatureData" :options="options" />
  </div>
  <div>
    <Line class="charts" :data="humidityData" :options="options" />
  </div>
</template>
<script lang="ts">
import {
  Chart as ChartJS,
  CategoryScale,
  LinearScale,
  PointElement,
  LineElement,
  Title,
  Tooltip,
  Legend
} from 'chart.js'
import { Line } from 'vue-chartjs'
import { humidityData, temperatureData, options } from './../chartConfig.js'

ChartJS.register(
  CategoryScale,
  LinearScale,
  PointElement,
  LineElement,
  Title,
  Tooltip,
  Legend
)

export default {
  components: {
    Line
  },
  data() {
    return {
      temperatureData,
      humidityData,
      options
    }
  }
}
</script>
<style lang="scss" scoped>
.charts {
  max-width: 100%;
}
</style>
