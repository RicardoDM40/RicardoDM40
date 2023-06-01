- 👋 Hi, I’m @Ricardo Dias de Melo
- 👀 I’m interested in learn codes
- 🌱 I’m currently learning javascript
- 💞️ I’m looking to collaborate on anyelse
- 📫 How to reach me: ricardodiasdemelo@gmail.com

<!---
RicardoDM40/RicardoDM40 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
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
          github_user_name: RicardoDM40
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
