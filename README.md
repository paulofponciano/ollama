# Labs com [Ollama](https://ollama.com/) rodando no EKS

## [Models](https://ollama.com/library)

## [Models - Hugging Face](https://huggingface.co/models)

<p align="center"><img src="https://ollama.com/public/ollama.png" width="150" alt="ollama"></p>

## Deploy with Helm

```sh
kubectl create ns ollama-ia
```
```sh
helm repo add ollama-helm https://otwld.github.io/ollama-helm/
helm repo update
```
```sh
helm upgrade --install ollama ollama-helm/ollama --namespace ollama-ia --values ollama-values.yaml
```

## Deploy Open WebUI with istio ingress

```sh
kubectl apply -f open-webui.yaml
```
---