apiVersion: apps/v1
kind: Deployment
metadata:
  name: web-page
  labels:
    app: web-page
spec:
  replicas: 2
  selector:
    matchLabels:
      app: web-page
  template:
    metadata:
      labels:
        app: web-page
    spec:
      containers:
      - name: web-page
        image: fabricioveronez/web-page:blue
        ports:
        - containerPort: 80
---
apiVersion: v1
kind: Service
metadata:
  name: web-page-service
spec:
  type: ClusterIP
  selector:
    app: web-page
  ports:
  - port: 80
    targetPort: 80
