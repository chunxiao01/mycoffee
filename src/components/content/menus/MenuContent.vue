<template>
  <div class="menu-content" ref="goodsGroupRef">
    <goods-group
      v-for="item in menuContentData"
      :goodsGroupData="item"
      :key="item.goodsGroupId"
      :currentGoodsTypeSelectedId="currentGoodsTypeSelectedId"
    ></goods-group>
  </div>
</template>

<script>
import GoodsGroup from "@/components/content/goods/GoodsGroup.vue"

export default {
  name: "MenuContent",
  props: {
    menuContentData: {
      type: Array,
      default() {
        return [
          {
            goodsGroupId: null,
            goodsGroupName: null,
            goodsGroupDesc: null,
            goodsGroupTypeType: [
              {
                goodsGroupTypeTypeId: null,
                goodsGroupTypeTypeName: null,
                goodsGroupTypeTypeNumber: null
              }
            ],
            goodsGroupDetailData: [
              {
                goodsid: null,
                goodspic: null,
                goodsname: null,
                goodstips: null,
                goodsdesc: null,
                goodsdescfill: null,
                goodsprice_new: null,
                goodsprice_old: null,
                goodsSelected: false,
                goodspieces: null,
                goodssellinfo: {
                  goodssellpic: null,
                  goodsinfopic: null,
                  goodsselltype: [
                    {
                      goodsselltypeId: null,
                      goodsselltypeName: null,
                      goodsselltypeDetails: [
                        {
                          goodsselltypeDetailId: null,
                          goodsselltypeDetailName: null,
                          goodsselltypeDetailMark: null,
                          goodsselltypeDetailSelect: false
                        }
                      ]
                    }
                  ]
                }
              }
            ]
          }
        ]
      }
    },
    currentGoodsTypeSelectedId: {
      type: String,
      default: null
    }
  },
  components: {
    GoodsGroup
  }
}
</script>

<style scoped></style>
