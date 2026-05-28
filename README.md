# Make a new project in Ximera

Use this repository to create a new Ximera project by clicking the "Use This Template" button in the upper right hand corner.

- Create your own github repo from this template; choose a proper name
- (automatically, an `action` will be started on github.com that in a few minutes deploys your repo on xerxes.ximera.org/demo-<your-githubname>-<yourgithubprojectname>).
- Go to https://overleaf.com, create a New Project, and choose 'Import from Github'
- (if not yet done: grant access to your github repos from Overleaf)
- Select your repo
- All done: edit eg newFolder/newActivity.tex, and select `Integrations->Github->Push Overleaf changes to Github'. After a few minutes, your demo-website will get the new version.

<img width="1489" height="776" alt="image" src="https://github.com/user-attachments/assets/335457e0-2f7c-42be-bfa1-3db798d690d8" />

Note:
- the `demo-<owner>-<repo>` site on xerxes is for demo/testing only. See `.github/workflows` for production-use. Any `demo-` website might (ie will) be deleted at some point.
- You can concurrently work with the repo in a Codespace, and/or on your local computer. BUT: you should pull/push regularly to prevent merge conflicts.
- only pdf compilations are possible on Overleaf, and they use the Overleaf TeX installations. The github actions and codespaces use the Ximera docker image that uses its own TeX version and also generates tha HTML version.

The key files for Ximera deployment are: 
- xmScripts (contains a configfile, and the script 'xmlatex' that is used to compile in the github action and codespace)
- global.css (for look on the web)
- .gitignore (to keep the folder-list and git-repo readable: skip logfiles etc)

## License
The contents of this repository (unless otherwise stated) are in the Public Domain.
