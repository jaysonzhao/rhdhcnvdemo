This repository contains helper scripts and template files for demo of RedHat Developer Hub integrating with OpenShift Virtualization. 
The demo is based on demo.redhat.com infrastructure provisioned. If you are running in your own environment, please be noted that you have to provision RHDH with Gitlab and ArgoCD before hand.

# rhpds 
## Selete the catalog as the demo base
![catalog](https://github.com/jaysonzhao/rhdhcnvdemo/blob/main/img/rhpds_demo.png?raw=true)

# create virtualization 
```
git clone https://github.com/jaysonzhao/rhdhcnvdemo.git
cd rhdhcnvdemo/scripts
chmod +x create_metal.sh
./create_metal.sh
```

![metalset](https://github.com/jaysonzhao/rhdhcnvdemo/blob/main/img/machineset.png?raw=true)


```
oc apply -f ./ocpvop.yaml
oc apply -f ./hyperconverged.yaml
```

![cnvenabled](https://github.com/jaysonzhao/rhdhcnvdemo/blob/main/img/cnvenabled.png?raw=true)


# import the template and create
## Find the GitLab and import the project
![importprj](https://github.com/jaysonzhao/rhdhcnvdemo/blob/main/img/templateproj.png?raw=true)

## Register the Postgresql VM template in catalog
![registertemplate](https://github.com/jaysonzhao/rhdhcnvdemo/blob/main/img/registerTemplate.png?raw=true)

# create component from template
![componentpage](https://github.com/jaysonzhao/rhdhcnvdemo/blob/main/img/provisionedvm.png?raw=true)

## You can find the VM config and console in a quick way.
![vmconfigpage](https://github.com/jaysonzhao/rhdhcnvdemo/blob/main/img/VMconfigpage.png?raw=true)
