kubectl get pod/notes-app-deployment-74fd7c85d9-mjl2h -o yaml -n test

kubectl describe pod/notes-app-deployment-74fd7c85d9-mjl2h  -n test

kubectl logs pod/notes-app-deployment-74fd7c85d9-mjl2h  -n test -f --tail 2


kubectl logs --previous pod/notes-app-deployment-564f464bf5-8vwzz -n test

kubectl logs --since=1h pod/notes-app-deployment-564f464bf5-8vwzz -n test

kubectl -n test logs pod/notes-app-deployment-564f464bf5-8vwzz   > pod.log 

kubectl exec -it pod/notes-app-deployment-74fd7c85d9-njm98 sh -n test

kubectl rollout restart deploy notes-app-deployment -n test

kubectl rollout restart deploy  -n test ------> all



kubectl exec pod/notes-app-deployment-564f464bf5-8vwzz -c notes-app-deployment apk add curl -n test

kubectl exec pod/notes-app-deployment-6c7c6d487-zvdpd -c notes-app-deployment curl http://127.0.0.1:3000 -n test

kubectl get pods -o wide -n test

kubectl get events -n test
-------------------------------------- Metrics
kubectl top po ------>  CPU(cores)   MEMORY(bytes) 
kubectl top no ------> nodes   ex: kubectl top po --namespace test

-------------------------------------- Debugging