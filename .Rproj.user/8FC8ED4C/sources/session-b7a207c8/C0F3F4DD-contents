#!/bin/bash

# Render full site
quarto render .

# Only commit if there are changes
if [ -n "$(git status --porcelain)" ]; then
  git add -f docs
  git commit -m "Site update: $(date '+%Y-%m-%d %H:%M:%S')"
  git push
else
  echo "No changes to commit"
fi