# Assignment_7
# Project 7 - WordPress Pentesting

Time spent: **X** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) VUlnerability Name or ID: Wordpress 2.5-4.6 - Authenticated Stored Cross-Site Scripting via Image Filename
  - [ ] Summary: Used wpscan to locate XSS vulnerability. Then look at steps to recreate. 
    - Vulnerability types:XSS
    - Tested in version: WP 4.2 
    - Fixed in version: WP 4.2.10
  - [ ] GIF Walkthrough: <a href="https://imgur.com/koN3Nea"><img src="https://i.imgur.com/koN3Nea.gif" title="source: imgur.com" /></a>
  - [ ] Steps to recreate: Login as admin. Go to create a page. Insert XSS into the headline of the page. View page. XSS will demonstrate. 
  - [ ] Affected source code: .....<div class="entry-content">
		<p class="p1"><span class="s1">&lt;IMG SRC=&#8221;#&#8221; ONERROR=&#8221;</span><span class="s2">alert(&#8216;XSS&#8217;)</span><span class="s1">&#8220;/&gt;</span></p>.....
			</div><!-- .entry-content -->
    - [Link 1](https://github.com/WordPress/WordPress/commit/c9e60dab176635d4bfaaf431c0ea891e4726d6e0)
1. (Required) Vulnerability Name or ID: WordPress  4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [ ] Summary: Script opens backdoor that gives attacker access to the site. 
    - Vulnerability types: XSS
    - Tested in version: WP 4.2
    - Fixed in version: WP 4.2.13
  - [ ] GIF Walkthrough: <a href="https://imgur.com/88S3nye"><img src="https://i.imgur.com/88S3nye.gif" title="source: imgur.com" /></a>
  - [ ] Steps to recreate: Find youtube video link to embed. Use the following code on the end x3csvg onload=alert(1)x3e’ Open backdoor to site.
  - [ ] Affected source code:<iframe width="560" height="315" src="’https://www.youtube.com/embed/fWeR6UhHRAM\x3csvg onload=alert(1)x3e’" frameborder="0" allowfullscreen></iframe>
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Required) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
