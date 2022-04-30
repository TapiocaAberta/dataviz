# SJC Digital: Data Visualization


Está é nossa página com aa visualização de dados abertos diversos!

## Criando dashboards

Em `dashboards` você encontra os dashboards em YML. Eles usam [Dashbuilder](https://www.dashbuilder.org/docs/#chap-dashbuilder-yaml-guides) para renderizar.

Simplesmente editor os dashboards e mande as mudanças para a branch main.


## Deploy



**Atualizando com novos dashboards**

* Edite `setup.js` para adicionar novos dashboards se tiver
* Commit o seu trabalho na main
* Faça merge com a main na branch dashbuilder
```
git checkout dashbuilder
git merge main
git push origin dashbuilder
```

**Atualizando a versão do Dashbuilder**

* Limpe a branch do dashbuilder e copie o novo conteúdo
```
git checkout dashbuilder
git reset main --hard
cp -r {caminho para o dashbuilder runtime} . 
rm setup.js
git add . -A
git commit -m 'Atualizando Dashbuilder'
git merge main
git push origin dashbuilder
```