<template functional>
  <div class="inline-flex flex-wrap w-full">
    <div v-for="(card, i) in props.list" :key="i" class="w-1/4 flex-auto border-2 m-2 bg-teal-100">
      <div class="border-b-2 p-2">{{ card.title }} <span class="float-right text-green-400">{{ i + 1 }}</span></div>
      <div class="border-b-2 p-2">
        <div class="pl-3" v-for="attribute in card.attributes" :key="attribute">{{ attribute }}</div>
      </div>
      <div class="p-2">{{ card.description }}</div>
    </div>
    <div class="w-1/4 flex-auto m-2"></div>
    <div class="w-1/4 flex-auto m-2"></div>
    <div class="w-1/4 flex-auto m-2"></div>
  </div>
</template>

<script>
export default {
  name: 'gallary-root',
  functional: true
}
</script>
