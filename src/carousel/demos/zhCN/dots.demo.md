# 指示点

设定 `dot-type` 来更改指示器的样式，可以使用 `never` 来隐藏指示点。

设定 `dot-placement` 来更改指示点的位置。

```html
<div>
  <n-radio-group v-model:value="type" style="margin-bottom: 10px;">
    <n-radio-button v-for="type in types" :key="type" :value="type">
      {{ type }}
    </n-radio-button>
  </n-radio-group>
</div>
<div>
  <n-radio-group v-model:value="placement" style="margin-bottom: 10px;">
    <n-radio-button
      v-for="placement in placements"
      :key="placement"
      :value="placement"
    >
      {{ placement }}
    </n-radio-button>
  </n-radio-group>
</div>
<n-carousel :dot-type="type" :dot-placement="placement" style="height: 240px;">
  <img
    class="carousel-img"
    src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel1.jpeg"
  />
  <img
    class="carousel-img"
    src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel2.jpeg"
  />
  <img
    class="carousel-img"
    src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel3.jpeg"
  />
  <img
    class="carousel-img"
    src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel4.jpeg"
  />
</n-carousel>
```

```js
import { defineComponent, ref } from 'vue'

export default defineComponent({
  setup () {
    const typeRef = ref('dot')
    const placementRef = ref('bottom')
    return {
      type: typeRef,
      types: ['dot', 'line', 'never'],
      placement: placementRef,
      placements: ['top', 'bottom', 'left', 'right']
    }
  }
})
```

```css
.carousel-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
```