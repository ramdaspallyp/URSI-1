# __Continuous Deployment/Delivery__
 ## __Docker Job: Docker Slave__ 
  __write a Dockerfile and Push to Github__
   1. clone docker file 
   ```
   git clone url(Dockerfile)
   ```
   1. Build image 
   ```
   docker image build -t gol:1.0 .
   ```
   3 docker image push docker Hub (any remote registry)
   ```
   docker login -u username -p password
   docker tag gol:1.0 abbanapuri0445/gol:1.0
   docker push abbanapuri0445/gol:1.0 
   ```
 ## __Kuberenets Job: K8s Slave__
  __write manifest file(abbanapuri0445/gol:1.0) and Push to GitHub__
   1. clone manifest 
   ```
   git clone url
   ```
   1. apply the manifest file to Kuberenets master
   ```
    kubectl apply -f deployment.yaml
    kubectl apply -f Service.yaml
   ```

### __CI__
  __CI stages , upto Jfrog artifactory__
![CI](./CI-stages.JPG)
### __CD__
  __CD stages docker and K8S__
![CD](./CD-new.JPG)