<template>
  <div>
    <div class="layout-padding">

      <p class="caption">
        Standalone
        <span class="label inline bg-secondary text-white">
          Model <span class="right-detail"><em>{{standalone.min}} to {{standalone.max}}</em> &nbsp;&nbsp;(0 to 50)</span>
        </span>
      </p>
      <q-double-range v-model="standalone" :min="0" :max="50"></q-double-range>

       <p class="caption">
        With Label
        <span class="label inline bg-secondary text-white">
          Model <span class="right-detail"><em>{{label.min}} to {{label.max}}</em> &nbsp;&nbsp;(-20 to 20, step 4)</span>
        </span>
      </p>
      <q-double-range v-model="label" :min="-20" :max="20" :step="4" label></q-double-range>

      <p class="caption">
        With Step
        <span class="label inline bg-secondary text-white">
          Model <span class="right-detail"><em>{{step.min}} to {{step.max}}</em> &nbsp;&nbsp;(0 to 45, step 5)</span>
        </span>
      </p>
      <q-double-range v-model="step" :min="0" :max="45" :step="5" label></q-double-range>

      <p class="caption">
        Snap to Step
        <span class="label inline bg-secondary text-white">
          Model <span class="right-detail"><em>{{snap.min}} to {{snap.max}}</em> &nbsp;&nbsp;(0 to 10, step 2)</span>
        </span>
      </p>
      <q-double-range v-model="snap" :min="0" :max="10" :step="2" label snap></q-double-range>

      <p class="caption">
        With Markers + Snap to Step
        <span class="label inline bg-secondary text-white">
          Model <span class="right-detail"><em>{{marker.min}} to {{marker.max}}</em> &nbsp;&nbsp;(-6 to 10, step 2)</span>
        </span>
      </p>
      <q-double-range v-model="marker" :min="-6" :max="10" :step="2" label snap markers></q-double-range>

      <p class="caption">
        Display Label Always
        <span class="label inline bg-secondary text-white">
          Model <span class="right-detail"><em>{{label.min}} to {{label.max}}</em> &nbsp;&nbsp;(-20 to 20, step 4)</span>
        </span>
      </p>
      <q-double-range v-model="label" :min="-20" :max="20" :step="4" label-always></q-double-range>



      <p class="caption">
        Drag Range
        <span class="label inline bg-secondary text-white">
          Model <span class="right-detail"><em>{{range.min}} to {{range.max}}</em> &nbsp;&nbsp;(0 to 100, step 1)</span>
        </span>
      </p>
      <q-double-range v-model="range" :min="0" :max="100" label drag-range></q-double-range>

      <p class="caption">
        Drag Range + Snap to Step
        <span class="label inline bg-secondary text-white">
          Model <span class="right-detail"><em>{{range.min}} to {{range.max}}</em> &nbsp;&nbsp;(0 to 100, step 5)</span>
        </span>
      </p>
      <q-double-range v-model="range" :min="0" :max="100" :step="5" drag-range label markers snap></q-double-range>

      <p class="caption">Disable Min + Drag Range</p>
      <q-double-range v-model="range" :min="0" :max="100" disable-min drag-range label></q-double-range>

      <p class="caption">Disable Max + Drag Range + With Step</p>
      <q-double-range v-model="range" :min="0" :max="100" :step="5" markers disable-max drag-range label-always></q-double-range>


      <p class="caption">Disabled State</p>
      <q-double-range v-model="standalone" :min="0" :max="50" disable></q-double-range>

      <p class="caption">Error State</p>
      <q-double-range class="has-error" v-model="standalone" :min="0" :max="50"></q-double-range>

      <p class="caption">Coloring</p>
      <q-double-range class="secondary" v-model="standalone" :min="0" :max="50" label></q-double-range>
      <q-double-range class="orange" v-model="standalone" :min="0" :max="50" label></q-double-range>
      <q-double-range class="dark" v-model="standalone" :min="0" :max="50" label></q-double-range>

      <p class="caption">Inside of a List</p>
      <div class="list">
        <div class="item two-lines">
          <i class="item-primary">local_atm</i>
          <div class="item-content">
            <q-double-range v-model="standalone" :min="0" :max="50" label></q-double-range>
          </div>
        </div>
        <div class="item two-lines">
          <i class="item-primary">euro_symbol</i>
          <div class="item-content">
            <q-double-range v-model="standalone" :min="0" :max="50" label></q-double-range>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      standalone: {
        min: 10,
        max: 35
      },

      step: {
        min: 10,
        max: 20
      },

      label: {
        min: -12,
        max: 8
      },

      snap: {
        min: 2,
        max: 6
      },

      marker: {
        min: 6,
        max: 8
      },

      range: {
        min: 20,
        max: 65
      }
    }
  }
}
</script>
