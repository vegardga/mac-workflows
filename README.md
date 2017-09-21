# tips
Diverse tips og triks i en ellers morsom data-hverdag.

## mac-workflows
Workflows til Mac.

## git

### Sette opp nytt git-prosjekt
Følg stegene under for å sette opp et nytt git-prosjekt:
0. Opprett nytt, tomt git-repository
1. Hent en klone av ønsket git-repository
2. Gå inn i denne mappen (i terminalen)
3. Utfør en mirror-push til det nye repositoryet
4. Gå ut fra mappen, og slett deretter den lokale mappen

Disse stegene kan oppsummeres med følgende kodelinjer:
```
$ cd $HOME
$ git clone --bare https://gitlab.com/the/path/to/my/old_repo.git
$ cd old_repo.git
$ git push --mirror https://gitlab.com/the/path/to/my/new_repo.git
$ cd ..
$ rm -rf old_repo.git
```

Mer informasjon her: https://help.github.com/articles/duplicating-a-repository/
