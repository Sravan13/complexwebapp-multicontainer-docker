# complexwebapp-multicontainer-docker

**Architecture in the development environment**
![complexApp](https://user-images.githubusercontent.com/5359534/80109143-c54f7c80-859a-11ea-9051-362f5219903c.PNG)

![complezapp2](https://user-images.githubusercontent.com/5359534/80109319-f8920b80-859a-11ea-8796-d60d60a78816.PNG)

![complezapp1](https://user-images.githubusercontent.com/5359534/80109281-ef08a380-859a-11ea-823e-e60b0413fb1b.PNG)

![complezapp3](https://user-images.githubusercontent.com/5359534/80109352-02b40a00-859b-11ea-8ae5-eb7e9dee58e3.PNG)

The project directory have single docker instance then EBS understand based on that file it will deploy application
![complezapp4](https://user-images.githubusercontent.com/5359534/80116055-20856d00-85a3-11ea-8ac6-c0cf973d344a.PNG)

Here we have multiple docker files then EBS confuse which one to take  for that reason "Dockerrun.aws.json" comes
![complezapp5](https://user-images.githubusercontent.com/5359534/80116058-21b69a00-85a3-11ea-9b8a-86760207857c.PNG)

Dockerrun.aws.json this file tell the EBS where to pull the images from , what resources to be allocated to each one , how to setup the port mapping and some associated information.this file Dockerrun.aws.json resembles as docker-compose file .compose have how to build the image but Dockerrun.aws.json have from where image to be pulled from.
![complezapp6](https://user-images.githubusercontent.com/5359534/80116061-224f3080-85a3-11ea-86a3-4aeab9d599d1.PNG)

EBS does not understand **Docker.aws.json** it is forward it Amazon Elastic  container service (ECS) which is responsible for creating the container based on  **Docker.aws.json** we provided . Follow amazon ECS task definition documention for writing  **Docker.aws.json**  .
![complezapp8](https://user-images.githubusercontent.com/5359534/80223307-bda8da00-8665-11ea-98f1-5581d2ff30fd.PNG)

![complezapp9](https://user-images.githubusercontent.com/5359534/80223321-c26d8e00-8665-11ea-8412-51bb100bb3eb.PNG)

**Production Architecture**
![complezapp11](https://user-images.githubusercontent.com/5359534/80237428-58131880-867a-11ea-9ee7-387e43ab869b.PNG)
![complezapp12](https://user-images.githubusercontent.com/5359534/80237432-59444580-867a-11ea-8b13-d794b5ae8b39.PNG)
![complezapp10](https://user-images.githubusercontent.com/5359534/80237434-59444580-867a-11ea-9bbb-a41b3d09383a.PNG)

Security group (Firewall rules ) tells what different sources of the internet can connect to different sources(instances) inside 
the VPC
