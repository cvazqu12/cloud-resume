# <center>Cloud Resume Challenge</center>

The Cloud Resume Challenge is a website that is built entirely within a cloud ecosystem, such as AWS or Azure, to demonstrate to employers the participants competencies and career readiness in the Cloud. For this challenge, my cloud resume uses AWS' suite of services. 

Chapter I, The Why:

What's the purpose of spending time on a project like this? I believe I have two good reasons:


1. Career-Readiness
With the cloud now being a more permanent enviornment, the demand for competent cloud engineers will only increase, and this project will make my bid to work in the cloud much more appealing.

2. LinkedIn

LinkedIn? What does this have to do a resume? It's simple; I don't like Linkedin. The social media site has been enstilled in high school and college students alike as a nessecary evil to succeed in this brave new world, but I don't agree with putting my resume on this site. The additional "need" to write lengthy blog posts or show off some achievement for career progression doesn't sit right with me, on top of privacy and data collection concerns. I hope to at least put the power of LinkedIn back into my own hands. 

Chapter II, The How:

What services did I choose to use? Quite a lot actually. Here is the list:

**<font color="lightblue">Frontend</font>**
* S3
* Cloudfront
* Route 53

**<font color="lightblue">Backend</font>**
* API Gateway
* Lambda
* Dynamo DB

**<font color="lightblue">CI/CD</font>**
* Github Actions
* Github Secrets
* Terraform

Let's break this down.

- Think of S3 as a folder that is hosted on the cloud without the need for anything else. It is considered a serverless service, because you don't need to worry about the underlying operating system it is running on. This portion helps with our Front-End development, as it holds the HTML, JS, and CSS.

- CloudFront helps with getting content to end users much faster by caching it in Edge locations (literally on the edge of a network). 

- Route 53 is Amazon's Domain Name Service that helps with pointing a domain name (christophervazquez.com) to the correct IP address, so end users will not have to memorize a string of numbers. This service will become even more crucial with the adoption of IPv6, which is a much longer address. 

- For this challenge, we needed to add something more than just a simple website. We decided on a visitor counter, that is shown at the bottom of the page. For each website visit, the visitor-counter ticks up one, but how do we keep track of that?

- Dynamo DB is Amazon's NoSQL database service. NoSQL refers to non-relational databases (in short, a database that has contents that you cannot put into a spreadsheet). It is also serverless. You will notice that many of these services are serverless, and that is because we do not need a full instance to make all of this work, in addition to that an instance with a full operating system is costly and comes with a higher need for maintanence. 

- Lambda is where we can write our counter that will communicate both with the website and Dynamo DB. This is serverless.

- The API Gateway's purpose is in the title. It is the software that allows the website to communicate with the Lambda program. We don't need to show the backend of our program, and in future cases, some portions may need to be kept secret. Having this barrier protects us. 

- GitHub Actions: This is part of our Infrastructure as Code portion of this challenge, which upgrades our manual processes into CI/CD, or Continus Intergration/Continuous Development. 

- GitHub Secrets is a secrets manager. To allow for CI/CD, we need to have a way to get access to the AWS account without using a normal password. Secrets allows us to use passthrough variables in our exposed public code, and the keys will be protected by Github. 

Chapter III, The Process: 

Overall, the experience was enjoyable. I am grateful that someone took the time to make this challenge a thing, and giving some of the guidelines on how to start in this brave new world. For the entirety of development, I used only flavors of Linux (no Mac, no Windows). I believe the use of Linux has made the completion of this project incredibly easy, since much of this project takes place in the command line. Of course, you can use a Mac or Windows computer to complete the job, but to open a new terminal quickly and almost entirely run through the later half of the project within VSC code and Terminal makes it incredibly easy and efficent to get this project finished. 

For the first half, I did choose to set it up manually for the first time, and it does take a lot of work to find your log in and go through the various menus, when the Terminal gives you no nonsense, no sensory overload. It's simple. 

I enjoyed the portion of using unit tests the most because this introduced to me a whole new way of implementing new code quickly, and reduces my need for a graphical interface. 


