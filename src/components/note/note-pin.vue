<template>
  <div class="ivu-sch-pin">
    <template v-for="item in pinList">
      <note-min :key="item.note_id" :pin-note="item" :note-id="item.note_id" :is_recycle="is_recycle"/>
    </template>
  </div>
</template>
<script>
import NoteMin from './note-min.vue'
export default {
  name: 'NotePin',
  props: {
    pinList: {
      type: Array,
      default: () => []
    },
    is_recycle: false
  },
  components: {
    NoteMin
  }
}
</script>
