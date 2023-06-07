# Script de Atualização de Tags de Recursos na Azure

## Descrição
Este script PowerShell permite atualizar as tags de recursos na plataforma Azure com base em um arquivo Excel fornecido. Ele automatiza o processo de atualização das tags para múltiplos recursos de forma eficiente.

## Pré-requisitos
- Módulo Az PowerShell instalado.
- Módulo ImportExcel instalado.
- Arquivo Excel contendo as tags e recursos.

## Uso
1. Clone este repositório para o seu ambiente local.
2. Certifique-se de ter instalado os módulos Az PowerShell e ImportExcel.
3. Abra o PowerShell e navegue até o diretório do repositório clonado.
4. Execute o script `Update-AzureTags.ps1` fornecendo as informações solicitadas:
   - Subscription ID: ID da assinatura da Azure.
   - Caminho completo do arquivo Excel: Caminho para o arquivo Excel contendo as tags e recursos.
   - Operation: Operação para atualização das tags ("merge", "delete" ou "replace").
5. Aguarde enquanto o script lê o arquivo Excel, obtém as informações dos recursos e atualiza as tags.
6. Após a conclusão, o script exibirá as tags atualizadas para cada recurso.
7. Verifique a Azure para confirmar as alterações nas tags dos recursos.

## Arquivo Excel
O arquivo Excel deve conter as seguintes colunas:
- Resource: Nome do recurso na Azure.
- OWNER: Proprietário do recurso.
- SUPPORT: Suporte do recurso.
- DESCRIPTION: Descrição do recurso.
- ENVIRONMENT: Ambiente do recurso.
- COST: Custo do recurso.
- CRITICAL: Criticidade do recurso.
- POWERSTART: Hora de início do recurso.
- POWERSTOP: Hora de parada do recurso.
- RESOURCEGROUP: Nome do grupo de recursos do recurso (opcional).

Certifique-se de preencher corretamente as informações de cada recurso na planilha Excel antes de executar o script.

## Contato
Para obter suporte ou fornecer feedback sobre o script, entre em contato com Carlos Marques (carlos.marques@4mstech.com).

---

Este script foi desenvolvido por Carlos Marques da Beyondsoft Brasil. Agradecemos seu interesse e esperamos que ele seja útil para suas necessidades de gerenciamento de tags de recursos na Azure.
