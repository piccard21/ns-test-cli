<template>
  <Page>
    <ActionBar title="Welcome to NativeScript-Vue!" android:flat="true" />
    <TabView
      android:tab-background-color="#53ba82"
      android:tab-text-color="#c4ffdf"
      android:selected-tab-text-color="#ffffff"
      android:selected:tab:highlight:color="#ffffff"
      :selected-index="selectedIndex"
      @selectedIndexChange="indexChange"
    >
      <TabViewItem title="Tab 1">
        <GridLayout columns="*" rows="*">
          <Label class="message" :text="msg" col="0" row="0" />
        </GridLayout>
      </TabViewItem>
      <TabViewItem title="Tab 2">
        <GridLayout columns="*" rows="*">
          <Label class="message" text="Tab 2 Content" col="0" row="0" />
        </GridLayout>
      </TabViewItem>
      <TabViewItem title="Tab 3">
        <GridLayout columns="*" rows="*">
          <Label class="message" text="Tab 3 Content" col="0" row="0" />
        </GridLayout>
      </TabViewItem>
    </TabView>
  </Page>
</template>

<script>
export default {
  data() {
    return {
      selectedIndex: 1,
      msg: "Hello World 21!",
      t01: {
        a: "asd",
        b: [1, 2, 3, 4],
        c: {
          d: 21,
          f: [122, 21, 21],
          g: {
            asd: 1
          }
        }
      }
    };
  },
  methods: {
    indexChange() {
      debugger;
      console.info("INDEX_CHANGE", this.t01);
    }
  }
};
</script>

<style scoped>
ActionBar {
  background-color: #53ba82;
  color: #ffffff;
}

.message {
  vertical-align: center;
  text-align: center;
  font-size: 20;
  color: #333333;
}
</style>
