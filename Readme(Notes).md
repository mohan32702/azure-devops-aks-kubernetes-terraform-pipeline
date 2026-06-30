 
 
 
Push Terraform Manifests
Your repo contains Terraform code that provisions infrastructure.
•	Ensure all Terraform manifests are committed
•	Push to your GitHub repository root path (use . as specified)

 <img width="940" height="394" alt="image" src="https://github.com/user-attachments/assets/e085edd0-9ab5-4a58-a589-6c00799d1c5a" />

 
Configure Azure Pipeline
Use azure-pipelines.yml to set up CI/CD in Azure DevOps.
File: azure-pipelines.yml
•	Pipeline is triggered from GitHub
•	SPN variable declared as runtime variable
•	Upload sshkey.pub and reference it in YAML

<img width="940" height="522" alt="image" src="https://github.com/user-attachments/assets/2ea723de-7369-44af-936c-d3775d226a59" />


 
Apply Terraform via Pipeline
Pipeline runs Terraform to provision cloud resources.
•	Validate manifests
•	Run terraform init, terraform plan, and terraform apply
•	Ensure SPN credentials are correctly passed

 
Deploy Kubernetes Objects
K8s objects are deployed through ArgoCD for GitOps workflow.
•	ArgoCD setup same as previous project
•	Point ArgoCD application to repo root (.)
•	Sync application to deploy workloads
 <img width="940" height="403" alt="image" src="https://github.com/user-attachments/assets/e061e8f1-d2e4-42ba-8a34-56276e6bfc3e" />

Argocd setup is done as same in previous project:
 
As our path is root in github so Please put(.) here
 <img width="940" height="601" alt="image" src="https://github.com/user-attachments/assets/9a383a17-4122-4476-8d49-a6dd365de274" />
<img width="940" height="517" alt="image" src="https://github.com/user-attachments/assets/a71c7fb9-44a8-43ef-8fe1-ed8b46567571" />

 
 
 
Verify Application Access
Final Check
Confirm that workloads are running and accessible.
•	Check pods and services in AKS cluster
•	Validate external access via LoadBalancer or Ingress
•	Confirm application endpoint is reachable
 <img width="940" height="484" alt="image" src="https://github.com/user-attachments/assets/d199fd51-2ba4-499e-a1c0-cbd5310d23d1" />


