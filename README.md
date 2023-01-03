# app-ecommere-docker-compose-new
jan/2023


install docker---start
install git
glone vote project
create 3 image vith docker file--dockerr build -t vote .
go worker app build with docker file
 crete result app with dockerfile


run redis db(docker run -d  --name redis redis)
run postgres db (docker run -d --name postgres -h postgres -e POSTGRES
                  USER=postgres -e POSTGRES_PASSWOR=postgress postgres)

create voting application
-----------
docker run -d -p 1000:80 --link redis:redis vote


create worker app
---------
docker run -d --link redis:redis --link postgres:db worker

we have 4 container

docker run -p 1001:80 --link postgres:db result

we have 5 container

