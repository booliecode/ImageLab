<template>
    <g
        :transform="`rotate(${this.rotate})`"
        :transform-origin="`${n.x + (n.width/2)}
        ${n.y + (n.height/2)}`">
      <g
        :id="n.id"
        :ref="n.id"
        :width="n.width"
        class="drag"
        @mousedown="dragMouseDown($event, n)"
        @touch:start="dragMouseDown($event, n)"
        >
      <g>
          <!-- eslint-disable -->
          <svg id="group1" 
            :width="n.width"
            :height="n.height"
            :x="n.x" :y="n.y"
            :transform-origin="`${n.x} ${n.y}`"
            :transform="`
            scale(${this.sx}, ${this.sy})
            translate(${this.mirror.x ? `-${this.n.width}` : '0'},
            ${this.mirror.y ? `-${this.n.height}` : '0'})`">
            <rect x="60" y="30" :width="n.width - 60" height="90"/>
            <rect x="40" y="20" style="fill:none;stroke:#FFFFFF;stroke-width:3;stroke-miterlimit:10;" :width="n.width - 50" height="90"/>
            <g id="layer1" transform="translate(-36.285713,-124.94062)">
              <path id="path1397" style="fill:#F39218;" d="M104.6,131.3c-34.2,0-62,27.8-62,62c0,0,0,0,0,0c0,34.2,27.8,62,62,62c34.2,0,62-27.8,62-62
                c0-2.2-0.1-4.3-0.4-6.5l-0.3,0.1l-4.2-4.8l-2.5,0.7l1.4,5.5l-4.5,1.2l-4.6-17.7l7.9-2.1c0.8-0.2,1.6-0.3,2.3-0.3
                C152.1,146.3,129.6,131.3,104.6,131.3z M149.2,172.3l4.6,17.7l-4.5,1.2l-1.8-7.1l-6.9,1.8l1.8,7.1l-4.5,1.2l-4.6-17.7l4.5-1.2
                l1.8,6.8l6.9-1.8l-1.8-6.8L149.2,172.3z M160.9,173.4c-0.4,0-0.8,0.1-1.2,0.2l-2.7,0.7l1.2,4.6l2.7-0.7c0.9-0.2,1.5-0.6,1.9-1
                c0.4-0.5,0.5-1.1,0.3-2c-0.2-0.9-0.6-1.4-1.2-1.6C161.6,173.5,161.3,173.4,160.9,173.4L160.9,173.4z M124.6,178.6
                c0.9,0,1.7,0.1,2.5,0.3c1.7,0.4,3.1,1.2,4.3,2.4s2,2.7,2.5,4.5c0.5,1.8,0.5,3.5,0,5.1c-0.5,1.6-1.3,3-2.6,4.1
                c-1.2,1.1-2.7,1.9-4.5,2.4c-1.8,0.5-3.5,0.5-5.2,0.1c-1.6-0.4-3.1-1.2-4.3-2.4c-1.2-1.2-2-2.7-2.5-4.5c-0.5-1.8-0.5-3.5,0-5.1
                c0.5-1.6,1.3-3,2.6-4.1c1.2-1.2,2.8-2,4.6-2.4C122.9,178.7,123.8,178.6,124.6,178.6L124.6,178.6z M124.5,183
                c-0.4,0-0.9,0.1-1.3,0.2c-0.9,0.2-1.7,0.7-2.3,1.3c-0.6,0.6-1.1,1.3-1.3,2.2c-0.2,0.9-0.2,1.8,0,2.8c0.3,1,0.7,1.8,1.3,2.5
                c0.6,0.6,1.4,1.1,2.2,1.3c0.9,0.2,1.7,0.2,2.7,0c0.9-0.2,1.7-0.6,2.3-1.2c0.6-0.6,1.1-1.3,1.3-2.2c0.2-0.9,0.2-1.8,0-2.8
                c-0.3-1-0.7-1.8-1.3-2.5c-0.6-0.6-1.3-1.1-2.2-1.3C125.3,183,124.9,183,124.5,183L124.5,183z M105.1,183.8l3.6,13.9l7.7-2l1,3.8
                l-12.2,3.2l-4.6-17.7L105.1,183.8z"/>
              <path id="path1403" style="fill:#020203;" d="M104.6,124.9c-37.7,0-68.3,30.6-68.3,68.3s30.6,68.3,68.3,68.3s68.3-30.6,68.3-68.3
                c0-1,0-2-0.1-3.1l10.7-2.8c7.5-1.9,12-9.6,10.1-17.1c-1.9-7.5-9.5-12-17-10.1l-10.8,2.8C154.7,140.5,131.5,124.9,104.6,124.9
                L104.6,124.9z M104.6,131.3c23.9,0,44.7,13.5,55,33.4l-58.3,15.1c-7.5,1.9-12,9.6-10.1,17.1c1.9,7.5,9.5,12,17,10.1l58.3-15.1
                c0,0.5,0,0.9,0,1.4c0,34.2-27.7,61.9-61.9,61.9s-61.9-27.7-61.9-61.9S70.4,131.3,104.6,131.3L104.6,131.3z M179,164.5
                c0.9,0,1.7,0.1,2.5,0.3c1.7,0.4,3.1,1.2,4.3,2.4c1.2,1.2,2,2.7,2.5,4.5c0.5,1.8,0.5,3.5,0,5.1c-0.5,1.6-1.3,3-2.6,4.1
                c-1.2,1.1-2.7,1.9-4.5,2.4c-1.8,0.5-3.5,0.5-5.2,0.1c-1.6-0.4-3-1.2-4.3-2.4c-1.2-1.2-2-2.7-2.5-4.5c-0.5-1.8-0.5-3.5,0-5.1
                c0.5-1.6,1.3-3,2.6-4.1c1.2-1.2,2.8-2,4.6-2.4C177.3,164.6,178.1,164.5,179,164.5L179,164.5z M178.8,168.9c-0.4,0-0.9,0.1-1.3,0.2
                c-0.9,0.2-1.7,0.7-2.3,1.3c-0.6,0.6-1.1,1.3-1.3,2.2c-0.2,0.9-0.2,1.8,0,2.8c0.3,1,0.7,1.8,1.3,2.5c0.6,0.6,1.4,1.1,2.2,1.3
                c0.9,0.2,1.7,0.2,2.7,0c0.9-0.2,1.7-0.6,2.3-1.2c0.6-0.6,1.1-1.3,1.3-2.2c0.2-0.9,0.2-1.8,0-2.8c-0.3-1-0.7-1.8-1.3-2.5
                c-0.6-0.6-1.3-1.1-2.2-1.3C179.7,169,179.3,168.9,178.8,168.9L178.8,168.9z M162,169.3c1,0,1.9,0.2,2.7,0.6c1.5,0.7,2.4,2.1,2.9,4
                c0.3,1.3,0.3,2.5,0,3.6c-0.3,1.1-1,2-1.9,2.7l4.7,5.4l-4.6,1.2l-4.2-4.8l-2.5,0.7l1.4,5.5l-4.5,1.2l-4.6-17.7l7.9-2.1
                C160.4,169.4,161.2,169.3,162,169.3L162,169.3z M149.2,172.3l4.6,17.7l-4.5,1.2l-1.8-7.1l-6.9,1.8l1.8,7.1l-4.5,1.2l-4.6-17.7
                l4.5-1.2l1.8,6.8l6.9-1.8l-1.8-6.8L149.2,172.3z M160.9,173.4c-0.4,0-0.8,0.1-1.2,0.2l-2.7,0.7l1.2,4.6l2.7-0.7
                c0.9-0.2,1.5-0.6,1.9-1c0.4-0.5,0.5-1.1,0.3-2c-0.2-0.9-0.6-1.4-1.2-1.6C161.6,173.5,161.3,173.4,160.9,173.4L160.9,173.4z
                M124.6,178.6c0.9,0,1.7,0.1,2.5,0.3c1.7,0.4,3.1,1.2,4.3,2.4s2,2.7,2.5,4.5c0.5,1.8,0.5,3.5,0,5.1c-0.5,1.6-1.3,3-2.6,4.1
                c-1.2,1.1-2.7,1.9-4.5,2.4c-1.8,0.5-3.5,0.5-5.2,0.1c-1.6-0.4-3-1.2-4.3-2.4c-1.2-1.2-2-2.7-2.5-4.5c-0.5-1.8-0.5-3.5,0-5.1
                c0.5-1.6,1.3-3,2.6-4.1c1.2-1.2,2.8-2,4.6-2.4C122.9,178.7,123.8,178.6,124.6,178.6L124.6,178.6z M124.5,183
                c-0.4,0-0.9,0.1-1.3,0.2c-0.9,0.2-1.7,0.7-2.3,1.3c-0.6,0.6-1.1,1.3-1.3,2.2c-0.2,0.9-0.2,1.8,0,2.8c0.3,1,0.7,1.8,1.3,2.5
                c0.6,0.6,1.4,1.1,2.2,1.3c0.9,0.2,1.7,0.2,2.7,0c0.9-0.2,1.7-0.6,2.3-1.2c0.6-0.6,1.1-1.3,1.3-2.2s0.2-1.8,0-2.8
                c-0.3-1-0.7-1.8-1.3-2.5c-0.6-0.6-1.3-1.1-2.2-1.3C125.3,183,124.9,183,124.5,183L124.5,183z M105.1,183.8l3.6,13.9l7.7-2l1,3.8
                l-12.2,3.2l-4.6-17.7L105.1,183.8z"/>
              <path id="path1365" style="fill:#FFFFFF;" d="M179,164.5c-0.9,0-1.7,0.1-2.6,0.4c-1.8,0.5-3.3,1.3-4.6,2.4c-1.2,1.1-2.1,2.5-2.6,4.1
                c-0.5,1.6-0.5,3.3,0,5.1c0.5,1.8,1.3,3.3,2.5,4.5c1.2,1.2,2.6,1.9,4.3,2.4c1.7,0.4,3.4,0.4,5.2-0.1c1.8-0.5,3.3-1.3,4.5-2.4
                c1.2-1.2,2.1-2.5,2.6-4.1c0.5-1.6,0.5-3.3,0-5.1c-0.5-1.8-1.3-3.3-2.5-4.5c-1.2-1.2-2.6-2-4.3-2.4
                C180.7,164.6,179.8,164.5,179,164.5L179,164.5z M178.8,168.9c0.4,0,0.9,0.1,1.3,0.2c0.8,0.2,1.6,0.6,2.2,1.3
                c0.6,0.6,1.1,1.4,1.3,2.5c0.3,1,0.3,2,0,2.8c-0.2,0.9-0.7,1.6-1.3,2.2c-0.6,0.6-1.4,1-2.3,1.2c-0.9,0.2-1.8,0.2-2.7,0
                c-0.8-0.2-1.6-0.6-2.2-1.3c-0.6-0.6-1.1-1.5-1.3-2.5c-0.3-1-0.3-1.9,0-2.8c0.2-0.9,0.7-1.6,1.3-2.2c0.6-0.6,1.4-1,2.3-1.3
                C177.9,169,178.4,168.9,178.8,168.9L178.8,168.9z M162,169.3c-0.8,0-1.6,0.1-2.5,0.3l-7.9,2.1l4.6,17.7l4.5-1.2l-1.4-5.5l2.5-0.7
                l4.2,4.8l4.6-1.2l-4.7-5.4c0.9-0.7,1.6-1.6,1.9-2.7c0.3-1.1,0.3-2.3,0-3.6c-0.5-2-1.5-3.3-2.9-4C163.9,169.5,163,169.3,162,169.3
                L162,169.3z M149.2,172.3l-4.5,1.2l1.8,6.8l-6.9,1.8l-1.8-6.8l-4.5,1.2l4.6,17.7l4.5-1.2l-1.8-7.1l6.9-1.8l1.8,7.1l4.5-1.2
                L149.2,172.3z M160.9,173.4c0.4,0,0.7,0,1,0.2c0.6,0.2,1,0.7,1.2,1.6c0.2,0.8,0.1,1.5-0.3,2c-0.4,0.5-1,0.8-1.9,1l-2.7,0.7
                l-1.2-4.6l2.7-0.7C160.1,173.5,160.5,173.4,160.9,173.4L160.9,173.4z M124.6,178.6c-0.9,0-1.7,0.1-2.6,0.4
                c-1.8,0.5-3.3,1.3-4.6,2.4c-1.2,1.1-2.1,2.5-2.6,4.1c-0.5,1.6-0.5,3.3,0,5.1c0.5,1.8,1.3,3.3,2.5,4.5c1.2,1.2,2.6,1.9,4.3,2.4
                c1.7,0.4,3.4,0.4,5.2-0.1c1.8-0.5,3.3-1.3,4.5-2.4c1.2-1.2,2.1-2.5,2.6-4.1c0.5-1.6,0.5-3.3,0-5.1c-0.5-1.8-1.3-3.3-2.5-4.5
                c-1.2-1.2-2.6-2-4.3-2.4C126.3,178.7,125.5,178.6,124.6,178.6L124.6,178.6z M124.5,183c0.4,0,0.9,0.1,1.3,0.2
                c0.8,0.2,1.6,0.6,2.2,1.3c0.6,0.6,1.1,1.4,1.3,2.5c0.3,1,0.3,2,0,2.8c-0.2,0.9-0.7,1.6-1.3,2.2c-0.6,0.6-1.4,1-2.3,1.2
                c-0.9,0.2-1.8,0.2-2.7,0c-0.8-0.2-1.6-0.6-2.2-1.3c-0.6-0.6-1.1-1.5-1.3-2.5c-0.3-1-0.3-1.9,0-2.8c0.2-0.9,0.7-1.6,1.3-2.2
                c0.6-0.6,1.4-1,2.3-1.3C123.6,183.1,124,183,124.5,183L124.5,183z M105.1,183.8l-4.5,1.2l4.6,17.7l12.2-3.2l-1-3.8l-7.7,2
                L105.1,183.8z"/>
            </g>
            <text x="180" y="80" style="fill:#FFFFFF;font-family:'Prompt'; font-weight: 600;font-size:25px;">{{settings.value}}</text>
          </svg>
          </g>
      </g>
    <ElementControlComp ref="sizeHelper" :rotate="rotate":n="n" :setpaddingside="10" :setpaddingtop="10" :lockEL="lockEL"/>
  </g>
</template>

<script>
import ElementMove from '../mixins/elementmove/mixin';
import ElementControlComp from '../mixins/elementcontrol/comp.vue';

export default {
  props: ['n', 'svg'],
  name: 'LohroBanderole',
  components: { ElementControlComp },
  mixins: [ElementMove],
  data: () => ({
    settings: {
      value: 'Banderole',
    },
    heightOrigin: 0,
    widthOrigin: 0,
    XOrigin: 0,
    YOrigin: 0,
  }
  ),
  methods: {
    getSettings(ref) {
      return [{
        id: '13337',
        name: 'text',
        type: 'text',
        value: this.settings.value,
        ref,
      }];
    },
    changeVal(name, value) {
      this.settings.value = value;
      return value;
    },
  },
};
</script>
