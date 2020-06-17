---
layout: home
---
<div class="py-12 bg-gray-100">
  {% include skills.html %}
  <div class="mx-3 md:w-1/2 md:mx-auto my-12 text-center">
    <a href="/abachiAbdeNasserCv.pdf" class="bg-green-500 text-white py-2 px-4 rounded">Download CV</a>
  </div>
    <div id="projects" class="projects flex flex-wrap justify-center items-start">
      {% for project in site.data.projects %}
      <a href="{{ project.url }}" class="project bg-white m-4 sm:w-3/4 md:w-1/3 lg:1/4 sm:p-4 sm:shadow-lg sm:rounded hover:opacity-75">
          <div>
              <img class="w-full h-64 object-cover object-center rounded" src="{{ project.image }}" alt="Image for {{ project.title }}">
          </div>
          <h2 class="font-semibold text-lg text-center mt-2">
              {{ project.title }}
          </h2>
          <div>
          <ul class="flex justify-center flex-wrap">
            {% for tech in project.technologies%}
            <li class="text-base font-semibold my-2 mx-3 bg-blue-200 px-2 py-1 rounded whitespace-no-wrap">{{ tech }}</li>
            {% endfor %}
          </ul>
          </div>
      </a>
      {% endfor %}
  </div>
</div>