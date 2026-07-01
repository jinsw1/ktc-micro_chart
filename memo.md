
# 우리가 만든 chart 를 압축해서 docs/ 폴더 안에 저장
helm package . -d docs/
# index.yaml 파일을 docs/ 폴더에 생성하기
helm repo index docs/ --url  https://oli999.github.io/micro_chart/
git add ./docs
git commit -m "release: member-app chart v1.0.1 package"
git push origin master