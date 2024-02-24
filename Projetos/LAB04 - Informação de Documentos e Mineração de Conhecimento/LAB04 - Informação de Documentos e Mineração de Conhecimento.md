# Laboratório 04 - Informação de Documentos e Mineração de Conhecimento

Neste laboratório foi necessário a criação e configuração de 2 recursos (Azure AI Services e Azure AI Search) e uma Storage Account.

Após a criação e configuração da Store Account, foi necessário a alteração do nível de acesso para anônimo.
Criei um Conteiner com o nome de _coffeereviews_ fiz o upload dos arquivos baixados do link [_zipped coffee reviews_](https://aka.ms/mslearn-coffee-reviews).

Com o ambiente configurado pude realizar a seguinte pesquisa:

Script utilizado:
  "search": "search=sentiment:'negative'"

Retorno:
```json
  {
  "@odata.context": "https://lab4busca.search.windows.net/indexes('azureblob-index')/$metadata#docs(*)",
  "value": [
    {
      "@search.score": 0.2876821,
      "content": "Review: Today I was truly disappointed with how long I had to wait for the pastries I ordered ahead of time. When I got my box, some of the pastries seemed stale. Terrible experience!  \nDate: October 23, 2018\nLocation: Chicago, Illinois \n\n",
      "metadata_storage_path": "aHR0cHM6Ly9sYWIwNG1hcmNvcy5ibG9iLmNvcmUud2luZG93cy5uZXQvY29mZmVlcmV2aWV3cy9yZXZpZXctOC5kb2N40",
      "locations": [
        "Chicago",
        "Illinois"
      ],
      "keyphrases": [
        "Terrible experience",
        "Review",
        "pastries",
        "time",
        "box",
        "Date",
        "October",
        "Location",
        "Chicago",
        "Illinois"
      ],
      "sentiment": "[\"negative\"]",
      "merged_content": "Review: Today I was truly disappointed with how long I had to wait for the pastries I ordered ahead of time. When I got my box, some of the pastries seemed stale. Terrible experience!  \nDate: October 23, 2018\nLocation: Chicago, Illinois \n\n",
      "text": [],
      "layoutText": [],
      "imageTags": [],
      "imageCaption": []
    }
  ]
}
```
