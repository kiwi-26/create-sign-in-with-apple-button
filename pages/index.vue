<template>
  <div class="section is-padding-lg">
    <div class="inner is-space">
      <h1 class="text is-xl is-strong">
        Create Sign in with Apple button
      </h1>

      <form class="grid is-gap-lg" @submit.prevent="submit">
        <div class="column is-mobile-12 is-tablet-8">
          <div class="grid is-gap-column-sm is-gap-row">
            <div class="column is-mobile-12">
              <h2 class="text is-lg is-strong">Size</h2>
            </div>
            <fieldset class="fieldset is-space-sm column is-mobile-12 is-tablet-6">
              <legend class="text is-strong">height</legend>
              <div class="box is-flex">
                <input type="number" name="height" v-model="height" min="30" max="64" class="input is-mobile-full">
              </div>
              <p class="text is-xs">Valid value: 30 - 64</p>
            </fieldset>
            <fieldset class="fieldset is-space-sm column is-mobile-12 is-tablet-6">
              <legend class="text is-strong">width</legend>
              <div class="box is-flex">
                <input type="number" name="width" v-model="width" min="130" max="375" class="input is-mobile-full">
              </div>
              <p class="text is-xs">Valid value: 130 - 375</p>
            </fieldset>
            <fieldset class="fieldset is-space-sm column is-mobile-12 is-tablet-6">
              <legend class="text is-strong">border radius</legend>
              <div class="box is-flex">
                <input type="number" name="border_radius" v-model="border_radius" min="0" max="50" class="input is-mobile-full">
              </div>
              <p class="text is-xs">Valid value: 0 - 50</p>
            </fieldset>
            <fieldset class="fieldset is-space-sm column is-mobile-12 is-tablet-6">
              <legend class="text is-strong">scale</legend>
              <div class="box is-flex">
                <input type="number" name="scale" v-model="scale" min="1" max="6" class="input is-mobile-full">
              </div>
              <p class="text is-xs">Valid value: 1 - 6</p>
            </fieldset>

            <div class="column is-mobile-12">
              <h2 class="text is-lg is-strong is-padding-top-sm">Style</h2>
            </div>
            <fieldset class="fieldset is-space-sm column is-mobile-12 is-tablet-6">
              <legend class="text is-strong">color</legend>
              <div class="box is-flex is-space-column-md is-middle">
                <div class="box">
                  <input class="input is-hidden" id="color-white" type="radio" value="white" v-model="color">
                  <label class="label is-space-column-xs" for="color-white">
                    <span class="radio"></span>
                    <span class="text">white</span>
                  </label>
                </div>
                <div class="box">
                  <input class="input is-hidden" id="color-black" type="radio" value="black" v-model="color">
                  <label class="label is-space-column-xs" for="color-black">
                    <span class="radio"></span>
                    <span class="text">black</span>
                  </label>
                </div>
              </div>
            </fieldset>
            <fieldset class="fieldset is-space-sm column is-mobile-12 is-tablet-6">
              <legend class="text is-strong">border</legend>
              <div class="box is-flex is-space-column-md is-middle">
                <div class="box">
                  <input class="input is-hidden" id="border" type="checkbox" name="border" v-model="border">
                  <label class="label is-space-column-xs" for="border">
                    <span class="checkbox"></span>
                    <span class="text">true</span>
                  </label>
                </div>
              </div>
            </fieldset>

            <div class="column is-mobile-12">
              <h2 class="text is-lg is-strong is-padding-top-sm">Wording</h2>
            </div>
            <fieldset class="fieldset is-space-sm column is-mobile-12 is-tablet-6">
              <legend class="text is-strong">type</legend>
              <div class="box is-flex is-space-column-md is-middle">
                <div class="box">
                  <input class="input is-hidden" id="type-sign-in" type="radio" value="sign-in" v-model="type">
                  <label class="label is-space-column-xs" for="type-sign-in">
                    <span class="radio"></span>
                    <span class="text">sign-in</span>
                  </label>
                </div>
                <div class="box">
                  <input class="input is-hidden" id="type-continue" type="radio" value="continue" v-model="type">
                  <label class="label is-space-column-xs" for="type-continue">
                    <span class="radio"></span>
                    <span class="text">continue</span>
                  </label>
                </div>
              </div>
            </fieldset>

            <fieldset class="fieldset is-space-sm column is-mobile-12 is-tablet-6">
              <legend class="text is-strong">locale</legend>
              <div class="box is-flex is-space-column-md is-middle">
                <div class="select">
                  <select v-model="locale">
                    <option value="en_US">en_US</option>
                    <option value="ar_SA">ar_SA</option>
                    <option value="ca_ES">ca_ES</option>
                    <option value="cs_CZ">cs_CZ</option>
                    <option value="da_DK">da_DK</option>
                    <option value="de_DE">de_DE</option>
                    <option value="el_GR">el_GR</option>
                    <option value="en_GB">en_GB</option>
                    <option value="es_ES">es_ES</option>
                    <option value="es_MX">es_MX</option>
                    <option value="fi_FI">fi_FI</option>
                    <option value="fr_CA">fr_CA</option>
                    <option value="fr_FR">fr_FR</option>
                    <option value="hr_HR">hr_HR</option>
                    <option value="hu_HU">hu_HU</option>
                    <option value="ja_JP">ja_JP</option>
                    <option value="id_ID">id_ID</option>
                    <option value="it_IT">it_IT</option>
                    <option value="iw_IL">iw_IL</option>
                    <option value="ko_KR">ko_KR</option>
                    <option value="ms_MY">ms_MY</option>
                    <option value="nl_NL">nl_NL</option>
                    <option value="no_NO">no_NO</option>
                    <option value="pl_PL">pl_PL</option>
                    <option value="pt_BR">pt_BR</option>
                    <option value="pt_PT">pt_PT</option>
                    <option value="ro_RO">ro_RO</option>
                    <option value="ru_RU">ru_RU</option>
                    <option value="sk_SK">sk_SK</option>
                    <option value="sv_SE">sv_SE</option>
                    <option value="th_TH">th_TH</option>
                    <option value="tr_TR">tr_TR</option>
                    <option value="uk_UA">uk_UA</option>
                    <option value="vi_VI">vi_VI</option>
                    <option value="zh_CN">zh_CN</option>
                    <option value="zh_HK">zh_HK</option>
                    <option value="zh_TW">zh_TW</option>

                  </select>
                </div>
              </div>
            </fieldset>
          </div>
        </div>

        <div class="column is-mobile-12 is-tablet-4">
          <div class="box is-flex is-padding-sm is-round">
            <button class="button is-plain is-primary is-mobile-0" type="submit">Create</button>
          </div>
          <div class="box is-flex is-center is-outline is-margin-horizontal-sm is-margin-top is-padding-vertical-sm preview">
            <img v-if="currentImage" :src="currentImage" />
          </div>
          <div class="box is-flex is-right is-sm is-padding-sm">
            <a class="button is-plain" :href="currentImage" target="_blank">Download image</a>
          </div>
          <div class="box is-margin-horizontal-sm is-margin-top">
            <ul class="list is-disc is-sm">
              <li class="item">
                <a href="https://developer.apple.com/documentation/signinwithapplejs/incorporating_sign_in_with_apple_into_other_platforms" target="_blank" class="text is-link is-primary" rel="noopener noreferrer">Official document</a>
              </li>
              <li class="item">
                <a href="https://twitter.com/koga_wiwi" target="_blank" class="text is-link is-primary" rel="noopener noreferrer">Ask about this tool</a>
              </li>
            </ul>
          </div>
        </div>
      </form>
    </div>
  </div>
</template>

<style scoped>
.preview {
  background: linear-gradient(45deg, #dddddd 25%, transparent 25%, transparent 75%, #dddddd 75%),
              linear-gradient(45deg, #dddddd 25%, transparent 25%, transparent 75%, #dddddd 75%);
  background-color: #ffffff;
  background-size: 30px 30px;
  background-position: 0 0, 15px 15px;
}
</style>

<script>
export default {
  data() {
    return {
      height: 30,
      width: 140,
      color: 'white',
      border: false,
      type: 'sign-in',
      border_radius: 15,
      scale: 1,
      locale: 'en_US',
      currentImage: null
    }
  },
  created () {
    this.currentImage = this.imageUrl()
  },
  methods: {
    submit() {
      this.currentImage = this.imageUrl()
      console.log(this.currentImage)
    },
    imageUrl() {
      const endpoint = 'https://appleid.cdn-apple.com/appleid/button?'
      let queries = [];
      queries.push(`height=${this.height}`)
      queries.push(`width=${this.width}`)
      queries.push(`color=${this.color}`)
      queries.push(`border=${this.border}`)
      queries.push(`type=${this.type}`)
      queries.push(`border_radius=${this.border_radius}`)
      queries.push(`scale=${this.scale}`)
      queries.push(`locale=${this.locale}`)
      return endpoint + queries.join('&')
    }
  }
}
</script>
