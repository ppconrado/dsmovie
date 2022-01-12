# ![DevSuperior logo](https://raw.githubusercontent.com/devsuperior/bds-assets/main/ds/devsuperior-logo-small.png) Semana Spring React - Episódio 3

> _Crie um app inédito para seu portfólio com as tecnologias mais demandadas do mercado_

## Realização

[DevSuperior - Escola de programação](https://devsuperior.com.br)

[![DevSuperior no Instagram](https://raw.githubusercontent.com/devsuperior/bds-assets/main/ds/ig-icon.png)](https://instagram.com/devsuperior.ig)
[![DevSuperior no Youtube](https://raw.githubusercontent.com/devsuperior/bds-assets/main/ds/yt-icon.png)](https://youtube.com/devsuperior)

## Objetivos do projeto para esta aula

- Integrar back end e front end
- Três pilares do React
  - Componentes
  - Props
  - Estado
- React Hooks
  - useState
  - useEffect
  - useParams
  - useNavigate

## AVISO: as aulas ficarão disponíveis somente até domingo às 23h59

## AVISO: Instruções sobre certificado no Github do [aqui](https://github.com/devsuperior/sds-dsmovie/tree/main/_certificado)

### Passo: Primeira requisição

- Instalar Axios

```bash
yarn add axios@0.24.0
```

- Definir BASE_URL
- Definir os tipos Movie e MoviePage
- Fazer a requisição

```typescript
export type Movie = {
  id: number;
  title: string;
  score: number;
  count: number;
  image: string;
};
export type MoviePage = {
  content: Movie[];
  last: boolean;
  totalPages: number;
  totalElements: number;
  size: number;
  number: number;
  first: boolean;
  numberOfElements: number;
  empty: boolean;
};
```

- **COMMIT: First request**

### Passo: React hooks: useState e useEffect

Hooks são funções cujo comportamento está vinculado ao estado e ao ciclo de vida do React a partir de componentes funcionais.
https://pt-br.reactjs.org/docs/hooks-overview.html

```
Hook: useState
Manter estado no componente
```

```
Hook: useEffect
Executar algo na instanciação ou destruição do componente, observar estado
```

- **COMMIT: useState, useEffect**

### Passo: Props

Props podem ser entendidas como argumentos do componente React.
https://pt-br.reactjs.org/docs/components-and-props.html
NOTA: em uma renderização dinâmica de coleção, cada elemento renderizado DEVE possuir um atributo `key`.

- **COMMIT: Props**

### Passo: useParams

- **COMMIT: useParams**

### Passo: Salvando score, useNavigate

Função para validar email

```javascript
// https://stackoverflow.com/questions/46155/whats-the-best-way-to-validate-an-email-address-in-javascript
export function validateEmail(email: any) {
  return String(email)
    .toLowerCase()
    .match(
      /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
    );
}
```

Objeto de configuração da requisição Axios

```
const config: AxiosRequestConfig = {
	baseURL: BASE_URL,
	method: 'PUT',
	url: '/scores',
	data: {
		email: email,
		movieId: movieId,
		score: score
	}
}
```

- **COMMIT: Save, useNavigate**

### Passo: Pagination

- **COMMIT: Pagination**

### Passo: Mostrar estrelinhas

- **COMMIT: Show score**
