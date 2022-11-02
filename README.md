### My Name is Olatunde and your welcome to My DevOps Season2 Episode1 Motion 

todays Focus 
# Docker ![image](https://user-images.githubusercontent.com/56154525/199482120-0a0f4270-ba2c-42da-b0c9-03e28ed9eeb7.png).

this project shows a freshly launched simple todo app list manager container running on Node.js built with Docker
it displays the very basics about building a container image and creating a Dockerfile to do so. Once the image is built, 
i proceeded to start with the container and saw the running app!

#Steps
after building my app with Nodejs i pushed it to github, 
on vs studio code which was the code editor i used you should see the package.JSON file and two subsidiaries which are the SRC folder and the SPEC folder

![image](https://user-images.githubusercontent.com/56154525/199478926-033c692f-095c-4445-b2d2-a5da916d9c06.png)

# Building the App's Container Image
to proceed further after building the application i added a docker file manually created which is suposed to help Build the App's Container Image
after manually creating the docker file i then added the followng lnes of code

FROM node:12-alpine
# Adding build tools to make yarn install work on Apple silicon / arm64 machines
RUN apk add --no-cache python2 g++ make
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]

make sure the Dockerfile does not have a file extension like .txt Some editors may append this file extension automatically and this would result in an error
once that s done we can then buld our container image 

# build the container image wth the following command in the terminal
docker build -t skills59 .

imidiately after that we can then proceed to start the container with the below command

# Start the App Container
docker run -dp 3000:3000 getting-started

After a few seconds, open your web browser to http://localhost:3000. You should see the app!

![image](https://user-images.githubusercontent.com/56154525/199482322-40df4949-52d2-4093-89f9-11685581f091.png)


If you take a quick look at the Docker Dashboard, you should see containers running.

Thanks for reading and practicing to be better with this. 


im also practicing to be better, kee it u and n no time your head will be there . 


