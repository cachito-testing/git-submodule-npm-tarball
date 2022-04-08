# git-submodule-npm

Repo for testing how Cachito handles [Git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules). <br/>
Such repos can be identified with `[submodule "<submodule path>"]` sections* in `.gitmodules`. <br/>

Also, it turns out that Cachito handles Git submodules better than Git itself does.
Git actually does not provide the contents inside of submodules in its [tarball](https://github.com/cachito-testing/git-submodule-npm/tarball/ab5482a3257f1d91d0e580fcdd51ba5fb325115b).
This particular case is handled with [another repository](https://github.com/cachito-testing/git-submodule-npm-tarball) which contains the same exact contents, but treats the submodule as a normal directory. <br/>

There are **3** of these repos - for package managers pip, npm, and Yarn: <br/>
1. [pip repo with a pip Git submodule](https://github.com/cachito-testing/git-submodule-pip) <br/>
2. **npm repo with a npm Git submodule** <br/>
3. [Yarn repo with a Yarn Git submodule](https://github.com/cachito-testing/git-submodule-yarn) <br/>

This particular repo is essentially [cachito-npm-without-deps](https://github.com/cachito-testing/cachito-npm-without-deps) containing [cachito-npm-with-deps](https://github.com/cachito-testing/cachito-npm-with-deps) as a submodule. <br/>
<br/>*`git-submodule-npm/.gitmodules`:
```
[submodule "cachito-npm-with-deps"]
	path = cachito-npm-with-deps
	url = https://github.com/cachito-testing/cachito-npm-with-deps.git
```
