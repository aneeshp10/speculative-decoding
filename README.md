<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a id="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/github_username/repo_name">
    <img src="src/frontend/public/golden-gate.png" alt="Logo" width="80" height="80">
  </a>

<h3 align="center">San Francisco StreetSense</h3>

  <p align="center">
    Not all routes are equal—StreetSense shows you how risk really changes along your walk in San Francisco.
    <br />
    <a href="https://github.com/aneeshp10"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/github_username/repo_name">View Demo</a>
    &middot;
    <a href="https://github.com/github_username/repo_name/issues/new?labels=bug&template=bug-report---.md">Report Bug</a>
    &middot;
    <a href="https://github.com/github_username/repo_name/issues/new?labels=enhancement&template=feature-request---.md">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-streetsense-san-francisco">About StreetSense San Francisco</a>
    </li>
    <li>
      <a href="#how-it-works-high-level">How It Works (High-Level)</a>
    </li>
    <li>
      <a href="#what-streetsense-is-and-isnt">What StreetSense Is (and isn’t)</a>
    </li>
    <li>
      <a href="#tech-stack">Tech Stack</a>
    </li>
    <li>
      <a href="#limitations">Limitations</a>
    </li>
    <li>
      <a href="#potential-improvements">Potential Improvements</a>
    </li>
    <li>
      <a href="#contributing">Contributing</a>
    </li>
  </ol>
</details>




<!-- ABOUT THE PROJECT -->
## About StreetSense San Francisco

[![Product Name Screen Shot][product-screenshot]](https://san-francisco-safety-index.vercel.app/)

StreetSense is a data-driven walking safety tool that helps people understand how risk changes along a route, not just where they start and end. It analyzes historical patterns across San Francisco at a block-level resolution, factoring in time of day and day of week to estimate expected risk for different paths. Instead of labeling neighborhoods as “safe” or “unsafe,” StreetSense surfaces how context and timing shape risk, giving users situational awareness as they plan their walk. The goal is not fear, but clarity—helping people make informed, confident choices about how they move through the city.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- GETTING STARTED -->
## Why StreetSense?
As a San Francisco resident, I’ve often noticed that how a walk feels can change dramatically depending on the time of day, even when the route itself stays the same. When commuting between two points, I’ve found myself weighing whether to walk, take public transit, or call a ride - not because of distance, but because of uncertainty about context. Existing maps optimize for speed, but they don’t help answer questions about situational risk. StreetSense grew out of wanting a more data-driven way to estimate expected risk for a given route, time, and day—so people can make more informed choices about how they move through the city.

- Walking risk isn’t uniform across a city or a route
- Time of day often matters more than distance
- Neighborhood-level labels hide important block-level variation
- Existing maps optimize for speed, not situational awareness

## How It Works (High-Level)
- Routes are broken into short segments using H3 geospatial indexing
- Each segment is scored using a machine-learning model trained on historical data based on location, day of the week, and time
- Scores are aggregated to highlight relatively higher and lower-risk portions of a route
- Results are visualized as a color-coded path overlay
  - 🟩 = Safe
  - 🟨 = Moderately Safe
  - 🟧 = Moderately Risky
  - 🟥 = Risky


## What StreetSense Is (and isn't)

**What It Is**
- A situational awareness tool
- A way to compare routes, not label places
- Time-sensitive and context-aware

**What It Is Not:**
- A *real-time* crime tracker
- A guarantee of safety
- A judgment of neighborhoods or people


## Tech Stack

- Backend: Python, Pandas, Numpy, FastAPI
- Machine Learning Modeling: XGBoost (Tweedie regression)
- Frontend: React + Vite, Google Maps API
- Geospatial indexing: H3
- Deployment: Vercel (frontend), Render (backend)

## Limitations

- Risk estimates are based on historical patterns, not real-time conditions.
- The model captures expected risk, not rare or unpredictable events.
- Scores are probabilistic and should be interpreted comparatively, not absolutely.
- Results may reflect reporting bias present in public incident data.

## Potential Improvements
- Experiment with different ML models and hyperparameter tuning
- Incorporate objective data we have on arrests made and degree of danger posed to fellow residents - this will help set the initial categorial scores better
- Batch route scoring to reduce latency and improve responsiveness.
- Precomputed risk maps by time bucket for faster lookups.
- Support for alternate routes optimized for lower expected risk.
- Extending the approach beyond San Francisco.

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/github_username/repo_name.svg?style=for-the-badge
[contributors-url]: https://aneeshpatil.bearblog.dev/
[forks-shield]: https://img.shields.io/github/forks/github_username/repo_name.svg?style=for-the-badge
[forks-url]: https://github.com/github_username/repo_name/network/members
[stars-shield]: https://img.shields.io/github/stars/github_username/repo_name.svg?style=for-the-badge
[stars-url]: https://github.com/github_username/repo_name/stargazers
[issues-shield]: https://img.shields.io/github/issues/github_username/repo_name.svg?style=for-the-badge
[issues-url]: https://github.com/github_username/repo_name/issues
[license-shield]: https://img.shields.io/github/license/github_username/repo_name.svg?style=for-the-badge
[license-url]: https://github.com/github_username/repo_name/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/aneesh-patil/
[product-screenshot]: images/streetsense_image.png
<!-- Shields.io badges. You can a comprehensive list with many more badges at: https://github.com/inttter/md-badges -->
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
