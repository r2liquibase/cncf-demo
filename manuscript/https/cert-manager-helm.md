# Use HTTPS With cert-manager And Helm

TODO: Intro

## Do

```bash
cat helm/app/templates/ingress.yaml

cat helm/app/templates/certificate.yaml

cat helm/app/values.yaml

yq --inplace ".tls.enabled = true" helm/app/values.yaml

helm upgrade --install cncf-demo helm/app --namespace dev --wait

kubectl --namespace dev \
    get issuers,certificaterequests,certificates,orders,secrets

echo "https://cncf-demo-dev.$DOMAIN"

# Open it in a browser
```

## Continue The Adventure

[Setup PostgreSQL DB](../db/README.md)
