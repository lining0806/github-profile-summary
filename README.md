## Docker for visualizing GitHub profiles

##### Build the Docker Images

	git clone https://github.com/lining0806/github-profile-summary.git
	cd github-profile-summary
	docker build -t lining0806/github-profile:latest .

##### Push the Docker Images

	docker login -u lining0806
	docker push lining0806/github_profile:latest
	docker logout

##### Pull the Docker Images

	docker pull lining0806/github_profile:latest

##### Run the Docker Container
	
	docker run -d --rm --name github-profile -p 7070:7070 lining0806/github-profile:latest
	docker run -d --rm --name github-profile -p 7070:7070 -e "TOKENS=mytoken1,mytoken2" lining0806/github-profile:latest

##### Then, you can visit http://your_hostname:7070

Demo： http://www.lining0806.com:7070/user/lining0806