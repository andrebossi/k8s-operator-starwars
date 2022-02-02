# Operator Startwars

### Build operator image
```bash
make docker-build docker-push IMG="dobolinux/starwars-operator:v0.0.2"
```
<br/>

### Deploy operator image manual
```bash
make deploy IMG="dobolinux/starwars-operator:v0.0.2"
```
<br/>

### instalação
```bash
kubectl apply -f config/manifests/bases/operator.clusterserviceversion.yaml
```
<br/>

### Para rodar o CI criar os secrets do seu repo no [Secrets Actions](https://github.com/andrebossi/k8soperator/settings/secrets/actions/new)
<br/>

### Example YAML resource
```yaml
apiVersion: lucasfilme.test.com/v1alpha1
kind: StarWars
metadata:
  name: starwars-sample2
  namespace: test-opeartor
spec:
  planeta: Naboo
  size: 1
```