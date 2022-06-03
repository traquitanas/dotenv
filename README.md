# Dotenv

<br>

O presente repositório tem a finalidade de aprender e testar o uso do `python-dotenv`.

<br>

O pacote [python-dotenv](https://pypi.org/project/python-dotenv/) serve para armazenar variáveis de ambiente. Segundo a descrição do _site_, temos que:

> Python-dotenv lê pares chave-valor de um arquivo .env e pode defini-los como variáveis de ambiente. Ajuda no desenvolvimento de aplicativos seguindo os [princípios de 12 fatores](https://12factor.net/).

<br>

O arquivo `.env` deve ter o seguinte formato:

```
SECRET_KEY=3333
DATABASE_PASSWORD=444
```

<br>

Até o momento, a melhor forma que encontrei de carregar as variáveis de ambiente, sem torna-las definitivas nas variáveis do PC, é:

```python
from dotenv import dotenv_values, find_dotenv

config = dotenv_values(find_dotenv(usecwd=True))
SECRET_KEY = config['SECRET_KEY']
```

<br>

---

### Referências

- https://www.youtube.com/watch?v=Jp5inslWuKg
