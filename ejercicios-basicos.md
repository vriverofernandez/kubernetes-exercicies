Estos son unos ejercicios sencillos. 
Necesitas terminar cada uno de ellos para pasar al siguiente ya que están relacionados.
Se parte desde una instalación de kubernetes ya realizada. Para ello se puede optar por minikube o multipass o alguna solución en la nube(EKS, AKS …) 

1.	Crea un namespace. Como nombre le pondremos frontend.
(Ayuda: https://kubernetes.io/es/docs/concepts/overview/working-with-objects/namespaces/)

2.	Verifica que funciona creando un deployment con una imagen de nginx y 2 réplicas y verificando que levantan y se quedan las dos en estado running. Crealo sobre el namespace que acabas de crear. 
(Ayuda: https://kubernetes.io/es/docs/concepts/workloads/controllers/deployment/)

3.	Realiza modificaciones sobre el deployment. Incrementa el número de replicas a 4, y añade los parámetros: maxSurge y maxUnavailable, ambos con valor de 50%.
(Ayuda: https://kubernetes.io/es/docs/concepts/workloads/controllers/deployment/)

4.	Crea un nuevo deployment de nombre nginx-nodeport. Crea un servicio de tipo NodePort para exponerlo a través del puerto 80.
Crea otro deployment de nombre nginx-clusterip y crea un servicio de tipo ClusterIp para exponerlo por el puerto 80.
Crea otro deployment de nombre nginx-loadbalancer y crea un servicio de tipo LoadBalancer para exponerlo.
