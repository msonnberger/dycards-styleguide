---
title: Accent Colors
styles: base/variables.scss
maturity: ready
control: exclude
colors: 
  - name: $indigo-200
    hex: '#C7D2FE'
  - name: $indogo-300
    hex: '#A5B4FC'
  - name: $indigo-500
    hex: '#6366F1'
  - name: $indigo-700
    hex: '#4338CA'
  - name: $indigo-800
    hex: '#3730A3'
  - name: $indigo-900
    hex: '#312E81'
  - name: $green
    hex: '#82E0AA'
  - name: $red
    hex: '#F1948A'
  - name: $white
    hex: '#FFF'
  - name: $black
    hex: '#000'
---
<style>
.set {
  display: flex;
  flex-wrap: wrap;
  margin: 0 -1rem;
  margin-top: 0;
  padding: 0;
  list-style: none;
}
li {
  flex: 1 0 20%;
  margin: 1rem;
}
.color {
  width: 100%;
  min-width: 160px;
  height: 80px;
  color: white;
  border: 1px solid whitesmoke;
  margin-bottom: 1rem;
}
p {
  margin: 0;
}
</style>
<ul class="set">
{% for item in page.colors %} 
  <li>
    <div class="color" style="background:{{ item.hex }}"></div> 
    <p>{{ item.name }}</p>
    {% if item.hex %}<p>{{ item.hex }}</p>{% endif %}
  </li>
{% endfor %}
</ul>