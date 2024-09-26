# Nginx Minikube Local Server

Este proyecto contiene la configuración de un servidor Nginx desplegado localmente en un clúster de Minikube.

## Descripción

Este repositorio contiene los manifiestos de Kubernetes (`.yaml`) para desplegar un pod con Nginx y un servicio tipo NodePort en un entorno local usando Minikube. Está pensado para ser un ejemplo básico de cómo implementar y exponer un servidor Nginx en un clúster de Kubernetes.

## Contenido

- `deploy-values.yaml`: Archivo de manifiesto de Kubernetes que define el pod de Nginx y el servicio para exponerlo a través de NodePort.

## Instrucciones

1. Instalar Minikube y Docker.
2. Clonar este repositorio.
3. Ejecutar `kubectl apply -f deploy-values.yaml` para desplegar el servidor Nginx.
4. Acceder al servicio a través del puerto definido en Minikube.

## Funciones adicionales

- **Resource Limits**: El pod Nginx tiene límites de recursos configurados para gestionar el consumo de memoria y CPU.
- **Readiness y Liveness Probes**: Se agregaron pruebas para verificar el estado del contenedor:
  - `readinessProbe`: Comprueba si el contenedor está listo para recibir tráfico.
  - `livenessProbe`: Comprueba si el contenedor está vivo y puede reiniciarlo si detecta problemas.


  ## Exitos L3
