# podman-quadlets
Examples/Demos showcasing the working of quadlets

To show the working of quadlets a simple example of Wordpress should be sufficient. We will use Wordpress and MySQL for now, simple enough to follow, but complex enough to demonstrate the power of Quadlets.

# Architeture 
WordPress demands a database, which can be used to connect to. This database must be running before WordPress is started. It might also be a good idea to put everything in a dedicated Podman Network

![image](https://github.com/user-attachments/assets/01697cf6-d557-4c70-a831-5224df03e184)


a WordPress network that holds the containers
a WordPress database container
a WordPress container
a volume per container
Therefore, we will need 5 Quadlets in total.


Place the service files in /etc/containers/systemd  dir and do a $ systemctl daemon-reload

Since we have maintained everything to depend on each other, we can start only the WordPress container and everything else should come up automagically.
systemctl start wordpress-app.service
