---
permalink: /trainee_program.html
layout: default
title: Research Software Trainees and Fellowships Program
---

We are looking for summer 2025 projects. Apply [here](https://docs.google.com/forms/d/e/1FAIpQLSei8ZRzL4hDXm-kaA8l5JSS053bi8nX42f3y4i56T3UkgBjYg/viewform?usp=dialog) or simply contact us if you are interested and have a project/mentor idea that fits our program. We are happy to discuss project ideas with you. 

## Research Software Trainees

  Are you a student or a recent grad interested in growing your software
skills by working on real open source research software projects used
by scientific researchers around the world? Would you like to work with
mentors actively involved in one of these open source projects?

People are the key to successful software. The HSF-India project aims to promote the
development of international research software collaborations in physics
by providing opportunities for undergraduate and graduate (both masters and PhD candidate)
trainees to connect with expert mentors from the particle physics, nuclear physics and astroparticle physics communities
as well as from the Computational/Data Science community.

Projects will follow a co-mentoring model allowing trainees to engage with
scientists in India, as well as the US and Europe.
At the same time, we aim to promote software as a collaborative activity and
encourage collaborations which engage individuals in ways that maximize their potential
and their potential impact on the community.
Trainees will spend their projects (flexible in length, but typically 3 or 6 months)
working to build their skills while working on an exciting and topical research software project.

### Who should apply to the HSF-India Trainees and Fellowships program?

Are you interested in building research software skills and gaining experience working as part of
a research team and contributing to cutting edge
open source research software projects? Then the HSF-India program could be for you.

This program is open to more experienced candidates as well as those new to scientific
software development. If you reasonably comfortable with basic programming through skills acquired (for example)
from coursework, dedicated training activities, and have some experience with prior research activities, you may be well suited for
one of the limited Fellowship opportunities. If not, we offer trainneeships for less experienced candidates that are excited to
engage with and work in a collaborative research environment.

Prior physics knowledge is helpful, but not required. We will also offer dedicated training
activities to help you improve specific software skills. Applications from women and members
of underrepresented groups in STEM activities are particularly encouraged.

Our program is open to candidates associated with institutions in India and in the US.

### What kind of research software projects are available?

  We are in the process of gathering research projects. You might have a project and mentor already in mind
  In that case, please be sure to include that information in your application. Our program will have three
  broad topical areas
  * [Analysis systems](/analysis_systems.html)
  * [Simulation methods](/simulation.html)
  * [Open science](/open_science.html)

however other project proposals are encouraged.
Follow the links for more details about each area. Expect projects to be software focused. Some projects
  will have a large focus on physics algorithms, others on computatonal methods. All aim to result in
  significant contributions to open source software and to build skills and knowledge as a result.

A list currently open available ideas can be found [here](http://research-software-collaborations.org/projects).

### How to apply
There is no requirement to establish a research project before applying, however having a mentor and potential topic area of mutual interest is beneficial. Our program will match selected students with mentors and projects, however the number of co-mentor teams will be limited. If you have interest in one or more specific
projects, please include that information as part of your application. We aim to match all
selected students to projects that they are excited about.

   * Deadline: April 1, 2024
   * Application form: [Please submit applications here](https://docs.google.com/forms/d/e/1FAIpQLSe56nh_uxU_1ge4zJihp6qzau6Cy5jIWerNxz4D3lhpynQGbw/viewform?usp=sf_link).
   * Application requirements:
      * CV summarizing academic background, work and research experiences, technical skills
      * Copy of recent academic transcripts
      * Statement of interests (1-2 pages maximum)
      * Letter of recommendation to be sent separately (optional but encouraged)
   * Questions:
      * Contact us by [email](mailto:rsc-inquiries@google-groups.com) with questions at any time.


{% assign trainees = site.pages | where: "pagetype", "trainee"
                               | last_name_sort: "name"
                               | reverse %}
{% assign active-trainees = trainees | select: "active" | where_exp: "item", "item.hidden != true" %}
{% assign inactive-trainees = trainees | reject: "active" | where_exp: "item", "item.hidden != true" %}


{%- if active-trainees.size > 0 %}
## Current Trainees

<div id="current" class="container-fluid">
  <div class="row">
    {% for person in active-trainees %}
      <div class="card" style="width: 12rem;">
         <img class="card-img-top" src="{{person.photo}}" alt="Card image cap">
         <div class="card-body d-flex flex-column">
           <div class="card-text">
              <b><a href="{{person.permalink}}">{{person.myname}}</a></b><br>
              <small>{{person.institution}}</small><br><br>
           </div>
           <div class="card-text mt-auto"><i>
             {% include fellow_dates.html dates=person.dates %}
           </i><br></div>
         </div>
      </div>
    {% endfor %}
  </div>
  <br>
</div>
{%- endif -%}

### Former trainees

  * This program is just starting. For examples of participants in other programs we are
  involved with, see the [IRIS-HEP fellows program](https://iris-hep.org/fellows.html)
  and the [HSF Google Summer of Code](https://hepsoftwarefoundation.org/activities/gsoc.html) program pages.

### Benefits of HSF-India
   * Gaining experience working in a unique scientific and collaborative environment
   * Learning new programming, research and analysis skills that are important for future careers in science and technology
   * Selected trainees will receive a token compensation ammount for their participation in the program

