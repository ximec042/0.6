```mermaid
sequenceDiagram
  Usuario->> Navegador: Escribe el texto y hace click en el botón send
  Navegador->> Servidor: Envia una solicitud  POST a la dirección new_note_spa
  Navegador->> Servidor: recibe el contenido y marca de tiempo de la nota como datos JSON
  Servidor->> Navegador: responde con un 201 created
  Servidor ->> Navegador: no envia más solicitudes HTTP, permanece en la misma página
