# Project 7 - WordPress Pen Testing

Time spent: 15 hours spent in total

> Objective: Find, analyze, recreate, and document 3 vulnerabilities affecting an old version of WordPress

## Pen Testing Report

### 1. Cross-site scripting (XSS)

- [ ] Summary: 
  - Tested in version: WordPress 4.2
  - Fixed in version: WordPress 4.2.34
- [ ] GIF Walkthrough:
- [ ]
   <img src="XSS.gif" width="800">
- [ ] Steps to recreate: 
  In the this attack I used "svg onload=alert(1)" in the comment section of the website
  
### 2. User Enumeration

- [ ] Summary:
  - Tested in version: WordPress 4.2
  - Fixed in version: WordPress 4.2.34
- [ ] GIF Walkthrough: 
- [ ] 
  <img src="Username_enum.gif" width="800">
- [ ] Steps to recreate: 
In this attack I used 
  "wpscan --url http://192.168.33.10 --api-token MY_TOKEN -e u vp" 
  in the terminal of my Kali machine to find a list of users on the website
  and saved it in the usernames.txt file.

### 3. Password Enumeration

- [ ] Summary: 
  - Tested in version: WordPress 4.2
  - Fixed in version: WordPress 4.2.34
- [ ] GIF Walkthrough: 
- [ ] 
  <img src="password_enum.gif" width="800">
- [ ] Steps to recreate: 
  In this attack I have created a password.txt file and stored a list of sample passwords in that file. 
  Then, I have performed the following command to find out passwords of the users: 
  wpscan --url http://192.168.33.10 --api-token MY_TOKEN --usernames username.txt --passwords password.txt


## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with  ScreenToGif

## Notes

Describe any challenges encountered while doing the work

I had some challenges with running and installing Vagrant
and downgrading WordPress version which later on successfully overcame

## License


    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
