# padrinoz_website

Toy website of the band "The Padrinoz" 🎸

> 🔄 work in progress....  🔄

# ReadMe

# MinisiteAWS
Template for mini-website with custom domain in AWS

This was done using R package `distill`

## Location
This is a template for creating a mini Project website deployed in Github, but with a custom domain in AWS  

+ Public link 2 AWS domain:  **https://thepadrinoz.com/**

## Steps to setup and launch new mini-site

1. on Github: Create new repo `whateverthename`
2. on Terminal (in the parent Local dir): Clone remote report 
	`git clone "https://github.com/lulliter/whateverthename.git"` 

3. on Local: Copy the content of example
   Then `git add -A` --> `git commit -m "message"`  --> `git push origin master`

4. on AWS: Go to route 53 and follow instructions to buy a domain (10$ per year) 
	`www.minisiteaws.net`

5. on AWS_Route53: domain registration should be done automatically 

6. a)  on AWS_Route53: in your route 53 dashboard, click hosted zones. It will provide you with a list of domain names you have with route 53. And then click the domain names you just created. Create an A type of record set. This will be your yourdomain.com rule. Keep everything the same. _{And add 192.30.252.153 and 192.30.252.154 in IPv4 address box. And save the record set.}_

> Actually  [GITHUB](https://help.github.com/en/articles/setting-up-an-apex-domain) says: 
A records that point your custom domain to the following IP addresses:
        + 185.199.108.153
        + 185.199.109.153
        + 185.199.110.153
        + 185.199.111.153


6. b)  Third, create another A type of record set. And this will be your www.yourdomain.com rule. And it will be an alias for yourdomain.com. Choose alias on the dashboard, from dropdown menu, choose yourdomain.com. Save the record set.

7. Last, go back to Github repository and create a file name CNAME and put in yourdomain.com in that file and save.


>>>>> 

4. on Github: Scroll down to the Repo / Setting/ Github Pages section 
	`click the drop down menu under “Source” and click “master branch”`

5. on Local: make some adaptation / add content 
6. (on Terminal/RStudio: Build the site locally (or see `./build_site.R`))
	+ actually, now the shell script `./_render-deploy.sh` invokes and run  `./build_site.R`
7. on Terminal/RStudio: git add/commit/push (or see `./_render-deploy.sh`)
	

>>>>> 

## TO do

+ check out [these](https://jhelvy.github.io/distillery/tips_and_tricks.html)
+ photos [istock](https://www.istockphoto.com/it/search/2/image?excludenudity=true&orientations=square&phrase=festival&sort=best&servicecontext=srp-related)
+ fontawsome [icons](https://fontawesome.com/icons/boombox?s=solid)
  

## Acknowledgments

+ This is "heavily" inspired by the beautiful website of [Ella Kaye](https://ellakaye.rbind.io/)
+ Followed instructions (clear and easy!) by D.YANG on  [Github Page with Route 53](https://danielyang1009.github.io/github-page-with-route-53-address/)
+ But also  from GITHUB on [custom domain for your GitHub Pages site](https://help.github.com/en/articles/setting-up-an-apex-domain)
+ ... more [Github + AWS (subdomain)](https://help.github.com/en/articles/setting-up-a-www-subdomain)
+ Another useful piece by Yeongho Kim on [types-of-github-pages](https://yeonghoey.com/github/pages/#types-of-github-pages)



