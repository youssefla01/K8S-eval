Premiere partie :
J'ai configuré l'environnement en définissant la variable d'environnement KUBECONFIG comme suit : export KUBECONFIG=/Users/hugomendes/cfa/k8s/kubeconfig.yml. 
Ensuite, j'ai procédé au déploiement d'un service et d'un pod pour les images redis et cloud.canister.io:5000/arhturescriou/node-redis. 
J'ai pris soin de modifier la valeur "value: redis://<address-of-base>" en "value: redis://redis-service-youssef:6379", en choisissant arbitrairement le port 6379.

Une fois les fichiers .yaml créés, j'ai utilisé la commande "kubectl apply -f nom_du_fichier.yaml" pour les appliquer. J'ai vérifié que les déploiements, 
les services et les pods se sont bien lancés en utilisant les commandes "kubectl get services" et "kubectl get pods".


Pour vérifier la communication entre mes services, j'ai exécuté la commande "kubectl get services", 
copié l'adresse IP externe suivie du port, puis collé cette URL dans mon navigateur. Dans mon cas, l'URL était http://37.59.31.40:6379/.
