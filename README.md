# mason-devops-test-answer
private repo for answering mason devops test

first Terraform script that sets up a 3-node OpenShift cluster on Vagrant
in file ```1-create-vargrant-to-run-openshift```

This will create three virtual machines in Vagrant, configure the necessary networking, and install OpenShift on the three nodes.
You can then access the OpenShift web console by navigating to https://<master-1-ip>:8443/console in your web browser.

secend set up oc 
In this example, we first configure the OpenShift provider with the necessary connection details, such as the API server URL and authentication token.
We then create a new project for our Kubernetes cluster using the openshift_project resource.
Next, we use the ```openshift_operator_installation``` resource to install the Kubernetes Operator on our OpenShift cluster.
We then define a Kubernetes custom resource definition (CRD) using the ```openshift_kubernetes_custom_resource_definition``` resource, which describes the desired state of our Kubernetes objects.
Finally, we create a new Kubernetes custom resource (CR) using the ```openshift_kubernetes_custom_resource``` resource, which creates an instance of our Kubernetes object within the OpenShift cluster.
Once you have defined this Terraform configuration, you can run ```terraform apply``` to provision your Kubernetes deployment on OpenShift Container Platform.

its on ```2-create-oc-cluster```

but there is an other solution that "not recomanded" is up and runing k8s cluster on oc
its on ```2.1-create-k8s-on-oc```

third is Setup a OpenEDX application in a kuberenete  
its on ```3-Setup-OpenEDX-in-k8s```

fourt is Create a gitlab CI/CD pipeline that commits to openEdx source code is automatically deployed to the cluster using FluxCD
In your GitLab repository, create a .gitlab-ci.yml file with the following contents: ```4-gitlab-ci```

fifth is grant flux to deploy on k8s cluster and connect it to gitlab repo
help on ```5-fluxcd-on-k8s-with-gitlab```


# devops-test
