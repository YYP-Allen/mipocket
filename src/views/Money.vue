<template>
  <Layout class-prefix="layout">
      <NumberPad/>
      <Types/>
      <Notes/>
      <Tags :data-source="tags"/>
    </Layout>
</template>

<script lang="js">
  import NumberPad from '@/components/Money/NumberPad.vue';
  import Types from '@/components/Money/Types.vue';
  import Notes from '@/components/Money/Notes.vue';
  import Tags from '@/components/Money/Tags.vue';
  export default {
    name: 'Money',
    components: {Tags, Notes, Types, NumberPad},
    data() {
      return {
        tags: ['住房', '餐饮', '交通', '通讯', '学习']
      }
    }
  };
</script>
<style lang="scss">
  .layout-content {
    display: flex;
    flex-direction: column-reverse;

  }
</style>
