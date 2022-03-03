### About me

Hi there, my name is Nikita Vokhmintsev . I am 23 years old, living and working in the city of Innopolis.
</br>
💻 I’m currently learning Python

### 📕 Courses

- Coursera - Basics of Python Programming

</br>
</br>

### 🔧 Technology Stack
[![Python](http://ForTheBadge.com/images/badges/Python.svg)](https://www.python.org/)
![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)

### Follow me

[![Telegram](https://img.shields.io/badge/Telegram-090909?style=for-the-badge&logo=telegram&logoColor=white)](https://www.t.me/sbrvrvl)
[![Instagram](https://img.shields.io/badge/Instagram-090909?style=for-the-badge&logo=Instagram&logoColor=white)](https://www.instagram.com/sbrvrvl)
[![Vkontakte](https://img.shields.io/badge/Vkontakte-090909?style=for-the-badge&logo=VK&logoColor=white)](https://vk.com/sbrvrvl)
[![Yandex Mail](https://img.shields.io/badge/yandex_mail-090909?style=for-the-badge&logo=appveyor&logoColor=white)](mailto:sbrvrvl@ya.ru)




# snk

[![GitHub marketplace](https://img.shields.io/badge/marketplace-snake-blue?logo=github&style=flat-square)](https://github.com/marketplace/actions/generate-snake-game-from-github-contribution-grid)
![type definitions](https://img.shields.io/npm/types/typescript?style=flat-square)
![code style](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)

Generates a snake game from a github user contributions graph

![](https://github.com/Platane/snk/raw/output/github-contribution-grid-snake.svg)

Pull a github user's contribution graph.
Make it a snake Game, generate a snake path where the cells get eaten in an orderly fashion.

Generate a [gif](https://github.com/Platane/snk/raw/output/github-contribution-grid-snake.gif) or [svg](https://github.com/Platane/snk/raw/output/github-contribution-grid-snake.svg) image.

Available as github action. Automatically generate a new image at the end of the day. Which makes for great [github profile readme](https://docs.github.com/en/free-pro-team@latest/github/setting-up-and-managing-your-github-profile/managing-your-profile-readme)

## Usage

**github action**

```yaml
- uses: Platane/snk@master
  with:
    # github user name to read the contribution graph from (**required**)
    # using action context var `github.repository_owner` or specified user
    github_user_name: ${{ github.repository_owner }}

    # path of the generated gif file
    # If left empty, the gif file will not be generated
    gif_out_path: dist/github-snake.gif

    # path of the generated svg file
    # If left empty, the svg file will not be generated
    svg_out_path: dist/github-snake.svg
```

> [example with cron job](https://github.com/Platane/Platane/blob/master/.github/workflows/main.yml#L24-L29)

**interactive demo**

<a href="https://platane.github.io/snk">
  <img height="300px" src="https://user-images.githubusercontent.com/1659820/121798244-7c86d700-cc25-11eb-8c1c-b8e65556ac0d.gif" ></img>
</a>

[platane.github.io/snk](https://platane.github.io/snk)

**local**

```
npm install

npm run dev:demo
```

## Implementation

[solver algorithm](./packages/solver/README.md)
