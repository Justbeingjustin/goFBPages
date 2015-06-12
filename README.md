goFBPages
======================
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/toomore/gogrs/master/LICENSE)

A facebook page photo album tool that supports concurrency download. This tool help you to download those photos for your backup, all the photos still own by original creator.

Install
--------------

    go get -u -x github.com/kkdai/goFBPages

Note, you need go to [faceook developer page](https://developers.facebook.com/tools/explorer?method=GET&path=me) to get latest token and update in "conf.json".

     TOKEN : "YOUR_TOKEN_HERE"

Usage
---------------------

    goFBPages [options] 

When [path...] is not given, "./" will be used as the default path for scanning files.


Options
---------------

- `-n` Facebook page name such as: [scottiepippen](https://www.facebook.com/scottiepippen).
- `-id` Facebook page id, if you know such as: 112743018776863 
- `-c=2` number of workers. (concurrency)


Examples
---------------

Download all photos from Scottie Pippen facebook pages

  goFBPages -n scottiepippen


Snapshot
---------------

![image](snapshot/1.png)

TODOs
---------------

- Support specific album download.
- Support firend/self album download for backup.

Inspired
---------------

This project inspired from [https://github.com/tzangms/iloveck101](https://github.com/tzangms/iloveck101). And I refer those implements as follow:

- Facebook graph API by Go: [https://github.com/huandu/facebook](https://github.com/huandu/facebook)
- Photo download: [https://github.com/lazywei/iloveck101](https://github.com/lazywei/iloveck101)


Contribute
---------------
Please open up an issue on GitHub before you put a lot efforts on pull request.

The code submitting to PR must be filtered with `gofmt`

License
---------------

This package is licensed under MIT license. See LICENSE for details.
