<template>
    <div class="app">
        <Split v-model="split1">
            <div slot="left" class="db-area">
                <div style="height: 25px;padding: 1px">
                    <Icon size="23" style=" float: right" type="md-add"/>
                </div>
                <Tree :data="data4" :render="renderContent" class="demo-tree-render"></Tree>
            </div>
            <div slot="right" class="key-value-area">
                <Split v-model="split2" style="offset: 1px">
                    <div slot="left" class="key-area">
                        <div style="height: 25px;padding: 1px;margin-left: 10px">
                            alpha
                        </div>
                        <div style="height: 25px;padding: 1px">
                            <Input suffix="ios-search" size="small" placeholder="Enter text" style="width: 100%"/>
                        </div>
                        <List border size="small" class="key-list">
                            <ListItem>This is a piece of text.</ListItem>
                            <ListItem>This is a piece of text.</ListItem>
                            <ListItem>This is a piece of text.</ListItem>
                            <ListItem>This is a piece of text.</ListItem>
                            <ListItem>This is a piece of text.</ListItem>
                            <ListItem>This is a piece of text.</ListItem>
                            <ListItem>This is a piece of text.</ListItem>
                            <ListItem>This is a piece of text.</ListItem>
                            <ListItem>This is a piece of text.</ListItem>
                            <ListItem>This is a piece of text.</ListItem>
                            <ListItem>This is a piece of text.</ListItem>
                            <ListItem>This is a piece of text.</ListItem>
                            <ListItem>This is a piece of text.</ListItem>
                            <ListItem>This is a piece of text.</ListItem>
                            <ListItem>This is a piece of text.</ListItem>
                            <ListItem>This is a piece of text.</ListItem>
                            <ListItem>This is a piece of text.</ListItem>
                            <ListItem>This is a piece of text.</ListItem>
                        </List>
                    </div>
                    <div slot="right" class="value-area">
                        Right Pane
                    </div>
                </Split>
            </div>
        </Split>
    </div>
</template>

<script>
  export default {
    name: 'landing-page',
    data () {
      return {
        data4: [
          {
            title: 'alpha',
            expand: true,
            selected: true,
            children: [
              {
                title: '0'
              },
              {
                title: '1'
              }
            ]
          },
          {
            title: 'pre',
            expand: true,
            selected: true,
            children: [
              {
                title: '0'
              },
              {
                title: '1'
              }
            ]
          }
        ],
        split1: 0.2,
        split2: 0.2
      }
    },
    methods: {}
  }
</script>

<style>
    @import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

    .app {
        width: 100%;
        height: 100vh;
        background: #f8f8f9;
    }

    .db-area {
        height: 100%;
        background: #f8f8f9;
    }

    .key-value-area {
        height: 100%;
    }

    .key-area {
        height: 100%;
        background: #f8f8f9;
    }

    .value-area {
        height: 100%;
        background: #f8f8f9;
    }

    .key-list {
        text-overflow: clip;
        overflow: hidden;
        white-space: nowrap;
        width: 100%;
        height: 100%;
    }

    ListItem {
        height: 10px;
    }
</style>
