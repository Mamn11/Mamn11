Hi, I am Mateus

<div>
 <img height="180em" src="https://github-readme-stats.vercel.app/api?username=Mamn11&show_icons=true&theme=dark&include_all_commits=true&count_private=true"/>
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Mamn11&layout=compact&langs_count=7&theme=dark"/>
<div>
  <div style="display: inline_block"><br>
  <img align="center" alt="" height="50" width="50" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" /> -
  <img align="center" alt="" height="50" width="50" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" /> -
  <img align="center" alt="" height="50" width="50" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg"/> -
  <img align="center" alt="" height="50" width="50" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg"/> - 
  <img align="center" alt="" height="50" width="50" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/android/android-original.svg"/>
          
          
name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: rafaballerini
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  
