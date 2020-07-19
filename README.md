# AWS_FACEDETECTION
This face detection app is using the telegram bot, services of AWS cloud such as EC2 instance, S3 and Amazon Rekognition. Overwiew of the project: The telegram bot will be used to upload the image to EC2, it will then store that particular image to S3, after this step Amazon rekognition will be invoked by S3 and it will identify the features from the image and return the count of the people in the image to the user as a reply of the input image.


STEP 1: Create a telegram bot usig botfather.
STEP 2: Create an EC2 instance on AWS cloud, I have made a linux based instance. To connect to the linux based instance. I have used PUTTY.
	Now connect to the virtual machine using Putty. Type is SSH and PORT is 22. Make a note of the IP address of your machine.You should have private key. 
	Public key will be with the instance and private key is needed in order to connect to the server. Convert pem to ppk using Puttygen.
	Now to connect to the VM copy the IP address and paste it on PUTTY. upload the PPK file under AUTH and click open.
	After that you will prompted for Username which is "ec2-user" on PUTTY Console. Then you will be successfully connected to your virtual machine.
	Now install the APACHE server in the VM. Command:
	sudo yum install httpd 		//download and install httpd
STEP 3: Upload the image from EC2 to S3 using PHP CODE1.
STEP 4: EC2 and Rekognition:
	- go to the running instance
	- Use CODE2 for rekognition run it and then rekognition will detect the number of faces.
	- To connect the telegram to your index.php page.. use (setwebhook) enter the bots access token and your url.
	-After setting webhook(https://api.telegram.org/bot{my_bot_token}/setWebhook?url={url_to_send_updates_to}) you can upload the image to telegram and it will directly uploaded to your EC2 and the faces will be detected.

