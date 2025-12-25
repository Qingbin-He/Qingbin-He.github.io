---
layout: page
title: Teaching
permalink: /teaching/
description: Overview of the courses I instruct for undergraduate and graduate students.
nav: true
nav_order: 5
---

<div class="cv">
  {% for entry in site.data.teaching %}
    <a class="anchor" id="{{ entry.title }}"></a>
    <div class="card mt-3 p-3">
      <h3 class="card-title font-weight-medium">{{ entry.title }}</h3>
      <div>
        {% if entry.type == "time_table" %}
          <ul class="card-text font-weight-light list-group list-group-flush">
            {% for item in entry.contents %}
              <li class="list-group-item">
                <div class="row">
                  <div class="col-xs-2 cl-sm-2 col-md-2 text-center" style="width: 75px">
                    {% if item.year %}
                      <span class="badge font-weight-bold danger-color-dark text-uppercase align-middle" style="min-width: 75px;">
                        {{ item.year }}
                      </span>
                    {% endif %}
                  </div>
                  <div class="col-xs-10 cl-sm-10 col-md-10 mt-2 mt-md-0">
                    {% if item.title %}
                      <h6 class="title font-weight-bold ml-1 ml-md-4">
                        {{ item.title }}
                      </h6>
                    {% endif %}
                    {% if item.institution %}
                      <h6 class="ml-1 ml-md-4" style="font-size: 0.95rem; font-style: italic;">
                        {{ item.institution }}
                      </h6>
                    {% endif %}
                    {% if item.description %}
                      <ul class="items">
                        {% for text in item.description %}
                          <li>
                            <span class="subitem">{{ text }}</span>
                          </li>
                        {% endfor %}
                      </ul>
                    {% endif %}
                  </div>
                </div>
              </li>
            {% endfor %}
          </ul>
        {% endif %}
      </div>
    </div>
  {% endfor %}
</div>

<div class="mt-5">
    <h3>Student Resources</h3>
    <div class="alert alert-info" role="alert">
        <i class="fa-solid fa-book-open mr-2"></i>
        <strong>Course Materials:</strong> Slides and assignments are available on <strong>Chaoxing (学习通)</strong> or the class <strong>WeChat Group</strong>.
    </div>
    <div class="alert alert-light border" role="alert">
        <i class="fa-solid fa-envelope mr-2"></i>
        <strong>Q&A:</strong> Please contact me via email (<code>highqb1993@163.com</code>) or visit my office by appointment.
    </div>
</div>
