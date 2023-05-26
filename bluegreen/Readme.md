
kubectl port-forward service/rollout-bluegreen-active 8081:8080 &
kubectl port-forward service/rollout-bluegreen-preview 8082:8080 &

localhost:8081
localhost:8082

kubectl get rollout -A
kubectl argo rollouts promote rollout-bluegreen

