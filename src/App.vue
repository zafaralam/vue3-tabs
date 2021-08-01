<script lang="ts">
import { defineComponent } from "vue";
import Tabs from "./components/Tabs.vue";
import Tab from "./components/Tab.vue";

export default defineComponent({
  name: "App",
  components: { Tabs, Tab },
});
</script>
<template>
  <h1>This is a <b>Tabs</b> example project with Vue 3 and Typescript</h1>
  <div class="tabs-example">
    <div class="example example-1">
      <h2>Example 1</h2>
      <p>
        This is the most basic way to use the Tabs component. The tab list will
        be show at the top and the names of the tabs are derived from the title
        prop of each Tab component.
      </p>
      <tabs>
        <tab title="Tab 1">
          <h3>This is Tab 1</h3>
        </tab>
        <tab title="Tab 2">
          <h3>This is Tab 2</h3>
        </tab>
      </tabs>
    </div>
    <div class="example example-2">
      <h2>Example 2</h2>
      <p>
        This example shows that the tab list items can be fully customized with
        there own icons if required.
      </p>
      <tabs>
        <template name="config">
          <div class="tab-title">
            <i class="ri-settings-3-fill" aria-hidden="true"></i>
            Config
          </div>
        </template>
        <tab title-slot="config">
          <h3>This is a config tab</h3>
        </tab>
        <tab title="Tab 2">
          <h3>This is Tab 2</h3>
        </tab>
      </tabs>
    </div>

    <div class="example example-3">
      <h2>Example 3</h2>
      <p>
        This example shows that the tab list items can be displayed at the
        bottom using the <b>reverse</b> prop on the Tabs component.
      </p>
      <tabs reverse>
        <template name="tab1">
          <div class="tab-title">
            <i class="ri-settings-3-fill" aria-hidden="true"></i>
            Config
          </div>
        </template>
        <template name="tab2">
          <div class="tab-title">
            <i class="ri-settings-3-fill" aria-hidden="true"></i>
            Tab 2
          </div>
        </template>
        <tab title-slot="tab1">
          <h3>This is a config tab</h3>
        </tab>
        <tab title-slot="tab2">
          <h3>This is Tab 2</h3>
        </tab>
      </tabs>
    </div>

    <div class="example example-4">
      <h2>Example 4</h2>
      <p>
        This example shows that the tab list can be shown vertically by using
        the <b>direction</b> prop on the Tabs component.
      </p>
      <tabs direction="vertical">
        <template name="tab1">
          <div class="tab-title">
            <i class="ri-settings-3-fill" aria-hidden="true"></i>
            Config
          </div>
        </template>
        <template name="tab2">
          <div class="tab-title">
            <i class="ri-settings-3-fill" aria-hidden="true"></i>
            Tab 2
          </div>
        </template>
        <tab title-slot="tab1">
          <h3>This is a config tab</h3>
        </tab>
        <tab title-slot="tab2">
          <h3>This is Tab 2</h3>
        </tab>
      </tabs>
    </div>

    <div class="example example-4">
      <h2>Example 5</h2>
      <p>
        This example shows that the tab list can be shown in the center or end
        by using the <b>position</b> prop on the Tabs component.
      </p>
      <tabs position="center">
        <template name="tab1">
          <div class="tab-title">
            <i class="ri-settings-3-fill" aria-hidden="true"></i>
            Config
          </div>
        </template>
        <template name="tab2">
          <div class="tab-title">
            <i class="ri-settings-3-fill" aria-hidden="true"></i>
            Tab 2
          </div>
        </template>
        <tab title-slot="tab1">
          <h3>This is a config tab</h3>
        </tab>
        <tab title-slot="tab2">
          <h3>This is Tab 2</h3>
        </tab>
      </tabs>
    </div>

    <div class="example example-4">
      <h2>Example 6</h2>
      <p>
        This example shows that the tab list can be shown in the center or end
        by using the <b>position</b> prop on the Tabs component.
      </p>
      <tabs position="end">
        <template name="tab1">
          <div class="tab-title">
            <i class="ri-settings-3-fill" aria-hidden="true"></i>
            Config
          </div>
        </template>
        <template name="tab2">
          <div class="tab-title">
            <i class="ri-settings-3-fill" aria-hidden="true"></i>
            Tab 2
          </div>
        </template>
        <tab title-slot="tab1">
          <h3>This is a config tab</h3>
        </tab>
        <tab title-slot="tab2">
          <h3>This is Tab 2</h3>
        </tab>
      </tabs>
    </div>
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  text-align: center;
  margin-top: 4px;
}

.tabs-example {
  display: grid;
  place-items: center;
  text-align: left;

  .example {
    width: 80%;
    padding: 0 1rem;
    border-radius: 8px;
    background: #fdfdff;
    border: 2px solid #e7e7f5;
    margin-block-end: 1rem;
  }
}
</style>
