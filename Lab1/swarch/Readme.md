# Laboratory #1
Juan Felipe Hernández Ochoa

## Lab development
In this Readme you can find the instructions to deploy the code using an envirioment for download the dependencies, an image describing the system structure of proyect and five properties of the system.

The system recreates a HUB create using flask library. In that HUB, you can insert a score of a subject for any person you might.

## Graphical representation

![If you can't see the image, you can find in the folder 'images'](/images/System_diagram.jpg)

## System properties

**Usability**

The system is very simple and intuitive. The web aplicaton guides the user throuht into the only two options for manage the subject score: insert and delete. Indicate what space is for what with simple layers and displays the inserted data on the screen for easy visualization

**Performance**

The system tasks quickly and efficiently. By using a lightweight base image with docker and separating the database into its own container. Since it only processes simple text and numbers without complex background logic, the response time for adding or deleting a student's score is almost instant.

**Scalability**

The systems is designed with a monolithic architectural style, becasue that, all the internal layers  are bundled tightly together. This means if the system needs to handle more activities, you cannot scale just one specific part of the code.

**Resilience**

The use of separate Docker containers makes the system more resilient. If the Python web application encounters an error and crashes, it will not bring down the MySQL database  because they run in isolated environments.

**High Availability**
While this is a simple local project, using Docker containers sets the foundation for a highly available system. By isolating the web application and the database into separate, independent containers, the system could easily be deployed to a cloud server in the future for examle.