# 🧠 Git Lab - Comandos Esenciales
------------------------------------------------------------
# 1️⃣ Inicializa el repositorio
git init
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@example.com"
echo "# Git Lab Comandos" > README.md
git add README.md
git commit -m "Primer commit"

# 2️⃣ Ciclo básico
git add .
git commit -m "Actualización de archivos"
git diff
git log --oneline

# 3️⃣ Ramas
git branch feature-x
git switch feature-x
git commit -am "Cambios en feature-x"
git switch main

# 4️⃣ Merge con conflicto
git merge feature-x
# Si hay conflicto, resuélvelo, luego:
git add .
git commit -m "Merge con resolución de conflicto"

# 5️⃣ Rebase interactivo
git rebase -i HEAD~3
# Combina o reordena commits según sea necesario

# 6️⃣ Stash
git stash
git switch main
git stash pop

# 7️⃣ Deshacer cambios
# Revert crea un commit inverso
git revert HEAD

# Reset mueve HEAD (peligroso)
git reset --hard HEAD~1
# ⚠️ Usa reset --hard solo en ramas desechables.

# 8️⃣ Recuperar commit con reflog
git reflog
git checkout <id_commit>

# 9️⃣ Trabajo con remotos
git remote add origin https://github.com/<usuario>/git-lab-comandos-<apellido>.git
git push -u origin main
git pull --rebase

# 🔟 Cherry-pick y bisect
git cherry-pick <id_commit>
git bisect start
git bisect bad
git bisect good <commit_anterior>
# Usa bisect para encontrar el commit que introdujo un bug.

# 11️⃣ Limpieza
git clean -n   # vista previa
git clean -fd  # elimina archivos no rastreados
# ⚠️ git clean -fd borra archivos permanentemente. Úsalo con precaución.

# 12️⃣ Etiquetas
git tag v1.0.0
git show v1.0.0

-------------------------------------------------------------
## 🧠 Fuentes oficiales
https://git-scm.com/docs
https://git-scm.com/book/es/v2
