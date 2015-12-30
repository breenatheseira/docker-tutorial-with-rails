### Running rails with docker:

!! Ensure that docker daemon is running first

1. Create rails app with 'rails new my-app'
2. Create Dockerfile and save it with:

FROM rails:onbuild

3. Build a Docker image: 
docker build -t my-app .

4. Start the rails server on port 8080 (accessible from local system's browser):
docker run -p 8080:3000 my-app

5. Open local system's browser and point to localhost:8080
