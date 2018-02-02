Step 1: cd at the root of the project. also change ports as per convenience in docker-compose.yml.

Step 2: sudo docker-compose up -d

Step 3: Run the setup-work.sh 
sudo ./setup-work.sh (it will download to the dependencies of Magento 2), in that part you will need the magento credentials, in the magento site https://marketplace.magento.com / customer / accessKeys /. After installation, it will mount in the src/ folder where all the files in Magento 2 will be.

--Note: Skip this step if you want to install magento setup from tar.gz, just extract the contents of setup archive in src/ folder

Step 4: Create your route on the sudo nano /etc/hosts hosts (change the MAGE_SETUP_BASE_URL = http: //it.mage-two/ in the .env file)

Step 5: Give permissions in the following sudo chmod -R 777 var/ generated/ pub/ media folders and in the chmod 755 auth.json file (if you are inside the docker container you do not need sudo commands)

Step 6: Access the percona in that case and phpmyadmin, (127.0.0.1:8888), enter the database and the core_config_data table and change http: //it.mage-two/ to your created host (do not forget the slash(/) at the end.)


                                                      ===Cheers===
