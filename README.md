- 👋 Olá, meu nome é @Vivisouzaa15
- 👀 Eu me interesso em escutar musicas, curtir momentos e sair com os amgs ...
- 🌱 Atualemtne, fasso o curso de informática no 1°ano ...
- 💞️ Estou curtindo minha vida com pessoas, amigos e familiares ...
  
![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=Vivisouzaa15&show_icons=true&theme=dracula)

<div style="display: inline_block"><br>
  <img align="center" alt="Vivisouzaa15-HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
  <img align="center" alt="Vivisouzaa15-CSS" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
  <img align="center" alt="Vivisouzaa15-Python" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
</div>
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


