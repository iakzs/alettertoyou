<script>
  let text = '';
  let emoji = '';
  let color = '#000000'; // Valor predeterminado para el color del texto
  let background = '#FFFFFF'; // Valor predeterminado para el color de fondo
  let background2 = '#FFFFFF'; // Valor predeterminado para el segundo color de fondo
  let title = '';
  let rainbow = false;
  let font = 'Delicious Handrawn'; // Valor predeterminado para la fuente

  function handleSubmit(event) {
    event.preventDefault();

    const url = `https://iakzs.is-a.dev/alettertoyou?text=${encodeURIComponent(text)}&emoji=${encodeURIComponent(emoji)}&color=${encodeURIComponent(color)}&background=${encodeURIComponent(background)}&background2=${encodeURIComponent(background2)}&title=${encodeURIComponent(title)}&israinbow=${encodeURIComponent(rainbow)}&font=${encodeURIComponent(font)}`;

    // Redireccionar al URL generado
    window.location.href = url;
  }
</script>

<style>
  h1 {
    font-family: 'Roboto', sans-serif;
    color: #333;
    text-align: center;
  }

  form {
    max-width: 400px;
    margin: 0 auto;
    padding: 20px;
    background-color: #f9f9f9;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }

  label {
    display: block;
    margin-bottom: 8px;
    font-family: 'Open Sans', sans-serif;
    font-size: 14px;
    color: #555;
  }

  input[type="text"],
  input[type="color"],
  select {
    width: 100%;
    padding: 8px;
    margin-bottom: 16px;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-family: 'Open Sans', sans-serif;
    font-size: 14px;
  }

  input[type="checkbox"] {
    margin-right: 8px;
  }

  button {
    display: block;
    width: 100%;
    padding: 10px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 4px;
    font-family: 'Open Sans', sans-serif;
    font-size: 16px;
    cursor: pointer;
  }
</style>

<h1>Customize alettertoyou</h1>
<form on:submit={handleSubmit}>
  <label for="title-input">Title:</label>
  <input type="text" id="title-input" bind:value={title}>
  
  <!-- Otros campos de entrada aquí... -->

  <button type="submit">Submit</button>
</form>
