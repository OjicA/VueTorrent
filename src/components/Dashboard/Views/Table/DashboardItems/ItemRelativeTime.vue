<script setup lang="ts">
import { Torrent } from '@/types/vuetorrent'
import dayjs from '@/plugins/dayjs'

defineProps<{ torrent: Torrent; value: (t: Torrent) => number }>()
</script>

<template>
  <span class="text-no-wrap">{{ dayjs(value(torrent) * 1000).fromNow() }}</span>
</template>
