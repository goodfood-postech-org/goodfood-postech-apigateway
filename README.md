# goodfood-postech-apigateway
Arquivos de configuração do AWS API Gateway

# Requisitos
- AWS CLI
- bash (Linux ou Git bash no Windows)
- Acessar a pasta da API correta no bach

# Exportar API
aws apigateway get-export \
    --rest-api-id 6c6lhva590 \
    --stage-name hmg \
    --export-type OAS30 openapi.yaml

# Exportar Documentation
aws apigateway get-documentation-parts \
    --rest-api-id 6c6lhva590 \
    --query 'items' \
    --output json > documentation.json

# Exportar Models
aws apigateway get-models \
    --rest-api-id 6c6lhva590 \
    --query 'items' \
    --output json > models.json