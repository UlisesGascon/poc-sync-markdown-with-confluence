# POC Synchronize Markdown files with Confluence

Proof of concept project aimed at enabling the automatic synchronization of Markdown files with Confluence

## 🔮 About

The [poc-sync-markdown-with-confluence](https://github.com/UlisesGascon/poc-sync-markdown-with-confluence) is a project or proof of concept (POC) that aims to synchronize markdown files with Confluence, an enterprise wiki tool. Markdown is a lightweight markup language commonly used for writing documents that can be easily converted to HTML. Confluence, on the other hand, is a powerful collaboration tool that allows teams to create, organize, and share content.

This POC explores the possibility of syncing markdown files, typically stored in a version control system like Git, with Confluence. The motivation behind this project is to streamline the content creation process and make it easier for teams to collaborate on documentation. With the ability to sync markdown files with Confluence, teams can continue using their preferred text editor and version control system while seamlessly updating and publishing content on Confluence.

There are several benefits to synchronizing markdown files with Confluence. First and foremost, it allows teams to leverage the simplicity and flexibility of markdown for content creation. Markdown is easy to learn and write, making it accessible to everyone on the team. Additionally, since markdown files are plain text, they can be easily versioned, compared, and merged using Git or any other version control system.

Overall, the poc-sync-markdown-with-confluence project offers a promising solution for organizations that want to centralize their documentation in Confluence while leveraging the strengths of markdown for content creation. By enabling synchronization between markdown files and Confluence, this POC aims to streamline the documentation workflow and enhance collaboration within teams.

### More information

This project POC uses the following tools:
- [mihaeu/cosmere](https://github.com/mihaeu/cosmere)
- [DavidAnson/markdownlint](https://github.com/DavidAnson/markdownlint)
- [igorshubovych/markdownlint-cli](https://github.com/igorshubovych/markdownlint-cli)

## 🧐 Demo

- This file: [Confluence](https://ulisesgascondemo.atlassian.net/wiki/spaces/syncmkdown/pages/360554/Sync+Markdown+files+with+Confluence) : [Markdown](https://github.com/UlisesGascon/poc-sync-markdown-with-confluence/blob/main/README.md)
- Simple Markdown to Confluence : [Confluence](https://ulisesgascondemo.atlassian.net/wiki/spaces/syncmkdown/pages/360561/Demo+Page+1+-+Simple+Markdown+to+Confluence) : [Markdown](https://github.com/UlisesGascon/poc-sync-markdown-with-confluence/blob/main/pages/demo1.md)
- Advance Markdown and Media to Confluence: [Confluence](https://ulisesgascondemo.atlassian.net/wiki/spaces/syncmkdown/pages/360568/Demo+Page+2+-+Advance+Markdown+and+Media+to+Confluence) : [Markdown](https://github.com/UlisesGascon/poc-sync-markdown-with-confluence/blob/main/pages/demo2.md)

## 📺 Tutorial

__soon__


## 📡 Usage

There are two pipelines in this project:
- [check-pr.yml](https://github.com/UlisesGascon/poc-sync-markdown-with-confluence/blob/main/.github/workflows/check-pr.yml) checks every file with a markdown linter on every pull request made against `main` branch.
- [publish.yml](https://github.com/UlisesGascon/poc-sync-markdown-with-confluence/blob/main/.github/workflows/publish.yml) same as `check-pr.yml` but also smart publishes the markdown files to Confluence.

## ⚙️ Customization

1. Fork this repository
2. Overwrite the `pages` folder content
3. Update the file `cosmere.json` with your `pages` and `baseUrl`
4. Add the following secrets to your repository `CONFLUENCE_USERNAME` and `CONFLUENCE_PASSWORD`.

Note: 
- `CONFLUENCE_PASSWORD` is yor API token, you can create one [here](https://id.atlassian.com/manage-profile/security/api-tokens).
- `CONFLUENCE_USERNAME` is your email address.