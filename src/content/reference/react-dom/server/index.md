---
title: APIs de servidor do React DOM
---

<Intro>

As APIs `react-dom/server` permitem que você renderize componentes React em HTML no servidor. Essas APIs são usadas apenas no servidor no nível mais alto de sua aplicação para gerar o HTML inicial. Um [framework](/learn/start-a-new-react-project#production-grade-react-frameworks) pode chamá-los para você. A maioria de seus componentes não precisa importar ou usá-los.
</Intro>

---

## APIs de servidor para Node.js Streams {/*server-apis-for-nodejs-streams*/}

Esses métodos estão disponíveis apenas nos ambientes com [Node.js Streams:](https://nodejs.org/api/stream.html)

* [`renderToPipeableStream`](/reference/react-dom/server/renderToPipeableStream) renderiza uma árvore React para um objeto encadeável [Node.js Stream](https://nodejs.org/api/stream.html).
* [`renderToStaticNodeStream`](/reference/react-dom/server/renderToStaticNodeStream) renderiza uma árvore React não interativa em um [Node.js Readable Stream.](https://nodejs.org/api/stream.html#readable-streams)

---

## APIs de servidor para Web Streams {/*server-apis-for-web-streams*/}

Esses métodos estão disponíveis apenas em ambientes com [Web Streams](https://developer.mozilla.org/pt-BR/docs/Web/API/Streams_API), que incluem navegadores, Deno, e alguns edge runtimes modernos:

* [`renderToReadableStream`](/reference/react-dom/server/renderToReadableStream) renderiza uma árvore React em uma [Readable Web Stream.](https://developer.mozilla.org/en-US/docs/Web/API/ReadableStream)

---

## APIs de servidor para ambientes sem streaming {/*server-apis-for-non-streaming-environments*/}

Esses métodos podem ser usados em ambientes que não possuem suporte a streams:

* [`renderToString`](/reference/react-dom/server/renderToString) renderiza uma árvore React em uma string.
* [`renderToStaticMarkup`](/reference/react-dom/server/renderToStaticMarkup) renderiza uma árvore React não interativa em uma string.

Esses métodos possuem funcionalidade limitada comparada com as APIs de streaming.

---

## APIs de servidor deprecadas {/*deprecated-server-apis*/}

<Deprecated>

Essas APIs serão removidas em uma futura versão major do React.

</Deprecated>

* [`renderToNodeStream`](/reference/react-dom/server/renderToNodeStream) renderiza uma árvore React em um [Node.js Readable stream.](https://nodejs.org/api/stream.html#readable-streams) (Deprecado.)
