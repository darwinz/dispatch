<template>
  <v-layout wrap>
    <div class="headline">Tags</div>
    <v-flex xs12>
      <v-layout column>
        <v-flex>
          <v-list two-line class="elevation-2">
            <v-list-group v-for="item in items" :key="item.id" no-action>
              <template v-slot:activator>
                <v-list-item>
                  <v-layout justify-space-around>
                    <v-flex xs3>
                      <v-list-item>
                        <v-list-item-action>
                          <v-icon>fa-user-circle</v-icon>
                        </v-list-item-action>
                        <v-list-item-content>
                          <v-list-item-title>{{ item.name }}</v-list-item-title>
                          <v-list-item-subtitle>Name</v-list-item-subtitle>
                        </v-list-item-content>
                      </v-list-item>
                    </v-flex>
                  </v-layout>
                </v-list-item>
              </template>
              <v-card-title primary-title>
                <div>{{ item.description }}</div>
              </v-card-title>
            </v-list-group>
          </v-list>
        </v-flex>
      </v-layout>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  name: "TagList",
  props: {
    items: {
      type: Array,
      default: null
    }
  },
  data() {
    return {}
  }
}
</script>
