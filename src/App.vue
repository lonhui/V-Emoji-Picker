<template>
  <div id="app">
    <VEmojiPicker :pack="pack" labelSearch="Pesquisar..." @select="selectEmoji" />
  </div>
</template>

<script>
import VEmojiPicker from './components/VEmojiPicker';
import packData from '../data/emojis.json';

export default {
  name: 'Demo',
  components: {
    VEmojiPicker
  },
  data: () => ({
    pack: packData
  }),
  methods: {
    selectEmoji(emoji) {
      console.log(emoji)
    }
  }
}
</script>
