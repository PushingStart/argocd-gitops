GIT LFS REPO SETUP

export REPO=clothing
git init && git lfs install && cp ../.gitattributes . && cp ../.gitignore . && git config user.name "Witt" && git config user.email "witt@baycity-roleplay.com" && git add .gitattributes && git add .gitignore && git add . && git commit -m "Initial Commit" && git remote add origin https://devops.pushingstart.com/BayCity%20Roleplay/Sandlot/_git/$REPO && git branch development && git switch development && git config lfs.https://devops.pushingstart.com/BayCity%20Roleplay/Sandlot/_git/$REPO.git/info/lfs.locksverify false && git push --set-upstream origin development


git init \
git lfs install \
cp ../.gitattributes . \
cp ../.gitignore . \
git config user.name "Witt" \
git config user.email "witt@baycity-roleplay.com" \
git add .gitattributes \
git add .gitignore \
git add . \
git commit -m "Initial Commit" \
git remote add origin https://devops.pushingstart.com/BayCity%20Roleplay/Sandlot/_git/$REPO \
git branch development \
git switch development \
git config lfs.https://devops.pushingstart.com/BayCity%20Roleplay/Sandlot/_git/$REPO.git/info/lfs.locksverify false \
git push --set-upstream origin development

git config pull.ff only

export GIT_TOKEN=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 && \
export GIT_REPO=https://github.com/PushingStart/argocd-gitops/tree/main/vault && \
argocd-autopilot app delete vault -p pushing-gitops


argocd-autopilot app create vault --app github.com/argoproj-labs/argocd-autopilot/examples/demo-app/ -p testing --wait-timeout 2m