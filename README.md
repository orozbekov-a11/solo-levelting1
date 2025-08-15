<!-- Профиль баннер -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00c6ff,100:0072ff&height=180&section=header&text=Hamza%20Works&fontSize=50&fontColor=ffffff&animation=fadeIn&fontAlignY=35" width="100%"/>

## 👋 Привет!
Я **Hamza** — увлечённый разработчик, люблю красивые и креативные проекты.  
Здесь ты найдёшь мои работы, эксперименты и код с душой.

---

## 🛠 Технологии и инструменты
<p align="center">
<img src="https://skillicons.dev/icons?i=html,css,js,react,nodejs,git,github,vscode,figma" />
</p>

---

## 📊 GitHub статистика
<p align="center">
<img src="https://github-readme-stats.vercel.app/api?username=HamzaWorks&show_icons=true&theme=tokyonight&hide_border=true" height="165"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=HamzaWorks&layout=compact&theme=tokyonight&hide_border=true" height="165"/>
</p>

---

## 🏆 GitHub Трофеи
<p align="center">
<img src="https://github-profile-trophy.vercel.app/?username=HamzaWorks&theme=tokyonight&no-frame=true&row=1&column=7" />
</p>

---

## 🐍 Змейка коммитов
![snake gif](https://github.com/HamzaWorks/HamzaWorks/blob/output/github-contribution-grid-snake.svg)

---

<!-- Нижний баннер -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0072ff,100:00c6ff&height=120&section=footer" width="100%"/>

name: Generate Snake

on:
  schedule:
    - cron: "0 */12 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: Platane/snk@v3
        with:
          github_user_name: HamzaWorks
          outputs: dist/github-contribution-grid-snake.svg
      - name: Push snake
        uses: EndBug/add-and-commit@v9
        with:
          message: "Generate snake"
          add: "dist/github-contribution-grid-snake.svg"
