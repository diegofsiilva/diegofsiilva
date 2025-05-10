<h1 align="left">Olá👋 Eu sou o Diego!</h1>

###

<p align="left">Estudante de Ciência Computação no Inteli, movido pela paixão por tecnologia e pelo propósito de transformar vidas por meio da educação.</p>

###

<h2 align="left">Linguagens</h2>

###

<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" height="40" alt="java logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="40" alt="python logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" height="40" alt="nodejs logo"  />
</div>

###

<h1 align="left">Curiosidades</h1>

###

<p align="left">⚽️ Gosto muito de esportes<br>🎸 Sou músico<br>💻 Fiz um curso técnico de informática no CEAP</p>

###

<h1 align="left">Meu Buddy</h1>

###

<p align="left">Meu buddy é o Guilherme, um estudante de Ciência da Computação que está trilhando seu caminho no Inteli ao meu lado.</p>

###

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=diegofsiilva&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=dracula&locale=en&hide_border=false&order=1" height="150" alt="stats graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=diegofsiilva&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=dracula&hide_border=false&order=2" height="150" alt="languages graph"  />
</div>




name: GitHub-Profile-3D-Contrib

on:
  schedule: # 03:00 JST == 18:00 UTC
    - cron: "0 18 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    name: generate-github-profile-3d-contrib
    steps:
      - uses: actions/checkout@v2
      - uses: yoshi389111/github-profile-3d-contrib@0.6.0
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          USERNAME: ${{ github.repository_owner }}
      - name: Commit & Push
        run: |
          git config user.name github-actions
          git config user.email github-actions@github.com
          git add -A .
          git commit -m "generated"
          git push

###
