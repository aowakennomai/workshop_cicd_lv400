# workshop_cicd_lv400
for workshop use

想把權限限縮在 bucket 的某一個目錄內，  
設定檔要改的地方如下，  
`s3` 增加 `upload-dir`  
`codedeploy` 調整 `key`  
差點被唬了 =___=

    deploy:
    - provider: s3
      upload-dir: deployment/20180926_lv400
    - provider: codedeploy
      key: deployment/20180926_lv400/workshop-${TRAVIS_BUILD_NUMBER}.zip
