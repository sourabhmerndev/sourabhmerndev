<h1 align="center">Hi 👋, I'm Sourabh</h1>
<h3 align="center">Learning MERN Stack | Full Stack Web Developer</h3>

<p align="left"> <a href="https://twitter.com/sxuxabh" target="blank"><img src="https://img.shields.io/twitter/follow/sxuxabh?logo=twitter&style=for-the-badge" alt="sxuxabh" /></a> </p>

<h3 align="left">Connect with me:</h3>
<p align="left">
<a href="https://twitter.com/sxuxabh" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/twitter.svg" alt="sxuxabh" height="30" width="40" /></a>
<a href="https://linkedin.com/in/https://www.linkedin.com/in/sourabh-k-mern-developer" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="https://www.linkedin.com/in/sourabh-k-mern-developer" height="30" width="40" /></a>
</p>

<h3 align="left">🚀 Tech Stack</h3>

<h4 align="left">Frontend</h4>
<p align="left">
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/> 
HTML &nbsp;&nbsp;&nbsp;

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> 
CSS &nbsp;&nbsp;&nbsp;

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> 
JavaScript &nbsp;&nbsp;&nbsp;

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" alt="react" width="40" height="40"/> 
React
</p>

<h4 align="left">Backend</h4>
<p align="left">
<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="nodejs" width="40" height="40"/> 
Node.js &nbsp;&nbsp;&nbsp;

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original-wordmark.svg" alt="express" width="40" height="40"/> 
Express.js &nbsp;&nbsp;&nbsp;

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg" alt="mongodb" width="40" height="40"/> 
MongoDB &nbsp;&nbsp;&nbsp;

</p>

<p><img align="left" src="https://github-readme-stats.vercel.app/api/top-langs?username=sourabhmerndev&show_icons=true&locale=en&layout=compact" alt="sourabhmerndev" /></p>

<p>&nbsp;<img align="center" src="https://github-readme-stats.vercel.app/api?username=sourabhmerndev&show_icons=true&locale=en" alt="sourabhmerndev" /></p>

<p><img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=sourabhmerndev&" alt="sourabhmerndev" /></p>


name: Generate snake game

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
      - uses: Sutil/snk@master
        id: snake-gif
        with:
          github_user_name: ${{ github.repository_owner }}
          svg_out_path: dist/github-contribution-grid-snake2.svg
          snake_color: 'blue'

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  
