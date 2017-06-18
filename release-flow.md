## Rough release flow

- npm run build
- npm run recommended-bump (lookup for recommended version bump i.e.: patch)
- cd src
- bump version manually to [VERSION]
- git add ./src/package.json
- cd ..
- bump version manually to [VERSION]
- git add ./package.json

- npm run changelog
- git add CHANGELOG.md
- git commit -m"docs(CHANGELOG): auto updated CHANGELOG.md"

- git commit -m"chore(release): [VERSION]"
- git tag [VERSION](i.e. 0.0.1)

- git push --follow-tags
- npm run github-release
- npm run release