<template>
  <div class="d-flex justify-center align-center flex-column" id="menu-solution">
    <v-container>
      <v-row>
        <v-col v-for="(item, i) in menuHeader" :key="i" cols="12" sm="6" md="3" class="pdnone">
          <p class="menu-title">
            {{ $t(item.title) }}
          </p>
          <p class="menu-subtitle">
            {{ $t(item.subtitle) }}
          </p>
        </v-col>
      </v-row>
    </v-container>
    <v-divider></v-divider>
    <v-container>
      <v-row>
        <v-col cols="12" sm="6" md="3">
          <ul class="list-item">
            <li v-for="(feature, index) in menuManager" :key="index">
              <nuxt-link :to="feature.link">
                <div class="icon-feature" :class="`bg-${feature.bgIcon}`">
                  <img
                      :src="require(`~/assets/images/icons/${feature.icon}`)"
                  />
                </div>
                <div class="d-flex flex-column">
                  <span class="item-title">{{ $t(feature.title) }}</span>
                  <span class="item-subtitle">{{ $t(feature.subtitle) }}</span>
                </div>
              </nuxt-link>
            </li>
          </ul>
        </v-col>
        <v-col cols="12" sm="6" md="3">
          <ul class="list-item">
            <li v-for="(feature, index) in menuOffice" :key="index">
              <a v-if="feature.link == '#'" href="#">
                <div class="icon-feature" :class="`bg-${feature.bgIcon}`">
                  <img
                      :src="require(`~/assets/images/icons/${feature.icon}`)"
                  />
                </div>
                <div class="d-flex flex-column">
                  <span class="item-title">{{ $t(feature.title) }}</span>
                  <span class="item-subtitle">{{ $t(feature.subtitle) }}</span>
                </div>
              </a>
              <nuxt-link :to="feature.link" v-else>
                <div class="icon-feature" :class="`bg-${feature.bgIcon}`">
                  <img
                      :src="require(`~/assets/images/icons/${feature.icon}`)"
                  />
                </div>
                <div class="d-flex flex-column">
                  <span class="item-title">{{ $t(feature.title) }}</span>
                  <span class="item-subtitle">{{ $t(feature.subtitle) }}</span>
                </div>
              </nuxt-link>
            </li>
          </ul>
        </v-col>
        <v-col cols="12" sm="6" md="3">
          <ul class="list-item">
            <li v-for="(feature, index) in menuAccounting" :key="index">
              <nuxt-link :to="feature.link">
                <div class="icon-feature" :class="`bg-${feature.bgIcon}`">
                  <img
                      :src="require(`~/assets/images/icons/${feature.icon}`)"
                  />
                </div>
                <div class="d-flex flex-column">
                  <span class="item-title">{{ $t(feature.title) }}</span>
                  <span class="item-subtitle">{{ $t(feature.subtitle) }}</span>
                </div>
              </nuxt-link>
            </li>
          </ul>
        </v-col>
        <v-col cols="12" sm="6" md="3">
          <ul class="list-item">
            <li v-for="(feature, index) in menuUtilities" :key="index">
              <nuxt-link :to="feature.link">
                <div class="icon-feature" :class="`bg-${feature.bgIcon}`">
                  <img
                      :src="require(`~/assets/images/icons/${feature.icon}`)"
                  />
                </div>
                <div class="d-flex flex-column">
                  <span class="item-title">{{ $t(feature.title) }}</span>
                  <span class="item-subtitle">{{ $t(feature.subtitle) }}</span>
                </div>
              </nuxt-link>
            </li>
          </ul>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import mixinMenu from '~/mixins/mixinMenu'

export default {
  name: "MenuSolution",
  mixins: [mixinMenu],
  data() {
    return {
      menuHeader: [
        {
          title: "menus.list_products.groups.dieu_hanh_quan_tri",
          subtitle:
              "H??? tr??? c??ng t??c ??i???u h??nh, t??c nghi???p v?? qu???n tr??? c???a doanh nghi???p.",
        },
        {
          title: "menus.list_products.groups.quan_ly_van_phong",
          subtitle:
              "H??? tr??? to??n di???n c??ng t??c qu???n l??, ????nh gi?? c??c ho???t ?????ng v??n ph??ng.",
        },
        {
          title: "menus.list_products.groups.nhan_su_ke_toan",
          subtitle:
              "H??? tr??? qu???n l??, ????nh gi??, t??nh l????ng, th?????ng, thu??? thu nh???p nh??n vi??n.",
        },
        {
          title: "menus.list_products.groups.tien_ich",
          subtitle:
              "C??c ti???n ??ch b??? tr??? n??ng cao tr???i nghi???m n???i b??? v?? ngo??i doanh nghi???p",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
