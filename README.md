# API Bin Checker

## Feito por [yFxZ](https://yfxz.xyz)
- API desenvolvida para ESTUDO, use da forma que bem entender.
    - API em PHP.
    - Resposta em JSON.
    - API construída em cima do site [Bincheck](https://bincheck.io).
- Um pouco sobre o desenvolvimento.
    - Foi feito puxando a *Response*, tinha alternativa de fazer usando Full cURL? Até tinha, porém nenhum payloader responde com os resultados.
- Como usar?
    - api?yfxz={bin}
- Use este exemplo: http://yfxz-bin.x10.mx/
    - Exemplo de resposta:
```json
{
  "🔒 Bin": "123456",
  "🏷️ Bandeira": "UATP",
  "💳 Tipo": "CREDIT",
  "🌟 Nível": "UATP",
  "🏦 Banco": "SHANDONG AIRLINES (SC)",
  "🌎 País": "CHINA",
  "🌎 Sigla": "CN",
  "💻 Coder": "yFxZ Dev's"
}
````

- Exemplo para usar a requisição da api em Pyhon:
```python
import requests
import os

os.system('cls')

def consultar_bin():
    bin_yfxz = input("Digite a BIN que deseja consultar: ")
    api_url = f"http://yfxz-bin.x10.mx/api.php?yfxz={bin_yfxz}"
    response = requests.get(api_url)
    
    if response.status_code == 200:
        data = response.json()
        print("\nInformações da BIN:")
        print("BIN:", data.get("🔒 Bin"))
        print("Bandeira:", data.get("🏷️ Bandeira"))
        print("Tipo:", data.get("💳 Tipo"))
        print("Nível:", data.get("🌟 Nível"))
        print("Banco:", data.get("🏦 Banco"))
        print("País:", data.get("🌎 Pais"))
        print("Sigla:", data.get("🌎 Sigla"))
        print("Coder:", data.get("💻 Coder"))
    else:
        print("Erro ao consultar a API.")

if __name__ == "__main__":
    consultar_bin()
```


### Acesse [yFxZ Hub](yfxz.store) 🍪


<div align="center">
  <img src="https://media.tenor.com/YcSbUdAyjy4AAAAi/cute-hello-kitty.gif" alt="Hello Kitty GIF">
</div>
