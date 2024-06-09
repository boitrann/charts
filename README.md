# Charts circle

## create chart
helm create my-chart    <!--create chart -->  
helm lint [CHART_PATH]  <!--test chart-->   
helm template release-name [CHART_PATH] -f values.yaml <!--view template-->  

## install/uninstall chart
helm ls  
helm install release-name [CHART_PATH]  
helm upgrade release-name [CHART_PATH] -f my-custom-values.yaml  

## packaging & uploading chart
helm package CHART_DIR -d target-dir  
helm repo index [CHART_PATH]  

## download & install/uninstall chart
helm repo add repo-name https://raw.githubusercontent.com/{my_username}/{my_repo}/{branch} <!--make repo public-->    
helm install release-name [CHART_PATH]  
helm uninstall release-name