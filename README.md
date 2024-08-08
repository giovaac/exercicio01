A. $ echo 01 > arquivo.txt
B. $ git add arquivo.txt
   $ git status
   On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   arquivo.txt
C. $ git commit -m "git add example - arquivo.txt"
[main (root-commit) ea92eea] git add example - arquivo.txt
 1 file changed, 1 insertion(+)
 create mode 100644 arquivo.txt
D. $ echo 02 > arquivo.txt
E. $ git diff
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02
F. $ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   arquivo.txt
G. $ git diff --staged
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02
H. $ echo 03 > arquivo.txt
I. $ git diff
diff --git a/arquivo.txt b/arquivo.txt
index 9e22bcb..75016ea 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-02
+03
J. $ git restore --staged arquivo.txt
K. $ git add arquivo.txt
@giovaac ➜ /workspaces/codespaces-blank/exer01 (main) $ git commit --m "Segundo commit arquivo.txt"
[main 050632a] Segundo commit arquivo.txt
 1 file changed, 1 insertion(+), 1 deletion(-)
   $ git log
commit 050632af8d82327010f08842a4763fbae843778d (HEAD -> main)
Author: Giovaac <giovanna.carvalho@aluno.faculdadeimpacta.com.br>
Date:   Thu Aug 8 00:47:53 2024 +0000

    Segundo commit arquivo.txt

commit ea92eea567966621476057ef0ac52ebcc57000e3
Author: Giovaac <giovanna.carvalho@aluno.faculdadeimpacta.com.br>
Date:   Thu Aug 8 00:37:41 2024 +0000
L. $ vi .gitignore
@giovaac ➜ /workspaces/codespaces-blank/exer01 (main) $ cat .gitignore
*.txt
   $ git add .gitignore
   $ git commit -m "Ignore"
[main 74adaf3] Ignore
 1 file changed, 1 insertion(+)
 create mode 100644 .gitignore
M. $ echo > novo.txt
   $ git status
On branch main
nothing to commit, working tree clean
   
