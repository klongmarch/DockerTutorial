Instructions from:
https://docs.docker.com/get-started/part2/

to run, do this:
docker build --tag=friendlyhello .

docker image ls

docker run -p 4000:80 friendlyhello

curl http://localhost:4000

Now let’s run the app in the background, in detached mode:
docker run -d -p 4000:80 friendlyhello

docker container ls

Share your image
$ docker login

docker tag image username/repository:tag

For example:

docker tag friendlyhello gordon/get-started:part2

$ docker image ls

Publish the image
Upload your tagged image to the repository:

docker push username/repository:tag

Pull and run the image from the remote repository
From now on, you can use docker run and run your app on any machine with this command:

docker run -p 4000:80 username/repository:tag

docker run -p 4000:80 gordon/get-started:part2
