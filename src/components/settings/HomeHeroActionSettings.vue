<template>
  <div class="container-transparent">
    <h2>Home Hero Action</h2>
    <p>Configuration of the Pega Mashup displayed when clicking on the "Learn more" button inside the Hero placement of the Home page</p>
    <div class="container">
      <div class="body">
        <div class="layout-labels-top layout-inline-grid-double">
          <div class="field-item">
            <label for="hero-action-action">Action</label>
            <select id="hero-action-action" v-model="settings.homeheroaction.action">
              <option>createNewWork</option>
              <option>display</option>
              <option>getNextWork</option>
              <option>openAssignment</option>
              <option>openWorkItem</option>
              <option>openWorkByHandle</option>
              <option>createNewWork</option>
            </select>
          </div>
          <div class="field-item">
            <label for="hero-action-actionparam">Action parameter</label>
            <input
              id="hero-action-actionparam"
              type="text"
              v-model="settings.homeheroaction.actionparam"
            />
          </div>
          <div class="field-item">
            <label for="hero-action-url">URL</label>
            <input id="hero-action-url" type="text" v-model="settings.homeheroaction.url" />
          </div>
          <div class="field-item">
            <label for="hero-action-objclass">Classname</label>
            <input id="hero-action-objclass" type="text" v-model="settings.homeheroaction.objclass" />
          </div>
          <div class="field-item">
            <label for="hero-action-startcase">Start case</label>
            <input
              id="hero-action-startcase"
              type="text"
              v-model="settings.homeheroaction.startcase"
            />
          </div>
          <div class="field-item">
            <label for="hero-action-application">Application name</label>
            <input
              id="hero-action-application"
              type="text"
              v-model="settings.homeheroaction.application"
            />
          </div>
          <div class="field-item">
            <label for="hero-action-pega_userid">Pega userid</label>
            <input
              id="hero-action-pega_userid"
              type="text"
              v-model="settings.homeheroaction.pega_userid"
            />
          </div>
          <div class="field-item">
            <label for="hero-action-pega_pwd">Pega password</label>
            <input
              id="hero-action-pega_pwd"
              type="password"
              v-model="settings.homeheroaction.pega_pwd"
            />
          </div>
        </div>
        <div class="layout-labels-top">
          <div class="field-item">
            <label for="hero-action-extraparam">Extra parameters (separated with comma)</label>
            <textarea id="hero-action-extraparam" v-model="settings.homeheroaction.extraparam" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mainconfig } from '../../global';

export default {
  data() {
    return mainconfig;
  },
};
</script>
