<template>
  <div class="tree-view-menu">
      <Tree-view-item :menus='menus'></Tree-view-item>
  </div>
</template>
<script>
import TreeViewItem from "./TreeViewItem";
// eslint-disable-next-line no-unused-vars
const menusData = [];
export default {
  components: {
    TreeViewItem
  },
  name: "TreeViewMenu",
  data() {
    return {
      menus: this.$store.state.menusModule.menus
    };
  }
};
</script>
<style scoped>
.tree-view-menu {
  height: 100%;
  overflow-y: auto;
  overflow-x: hidden;
}
.tree-view-menu::-webkit-scrollbar {
  height: 6px;
  width: 6px;
}
.tree-view-menu::-webkit-scrollbar-trac {
  -webkit-box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
  box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
}
.tree-view-menu::-webkit-scrollbar-thumb {
  background-color: #6e6e6e;
  outline: 1px solid #333;
}
.tree-view-menu::-webkit-scrollbar {
  height: 4px;
  width: 4px;
}
.tree-view-menu::-webkit-scrollbar-track {
  -webkit-box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
  box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
}
.tree-view-menu::-webkit-scrollbar-thumb {
  background-color: #6e6e6e;
  outline: 1px solid #708090;
}
</style>
