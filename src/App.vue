<template>
  <div id="app">
    <main class="flexbox">
      <Board id="board-1">
        <Card id="card-1" draggable="true">
          <p>Card 1 - draggable</p>
        </Card>
      </Board>

      <Board id="board-2">
        <Card id="card-2" draggable="true">
          <p>Card 2 - not draggable</p>
        </Card>
        <Card id="card-3" draggable="true">
          <p>Card 3 - not draggable</p>
        </Card>
        <Card id="card-4" draggable="true">
          <p>Card 4 - draggable</p>
        </Card>
      </Board>
      <Board id="board-3"></Board>
      <Board id="board-4"></Board>
    </main>

  </div>
</template>

<script>
import Board from "./components/Board";
import Card from "./components/Card";
export default {
  name: 'App',
  components: {
    Board,
    Card
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  background-color: #eee;
}

.flexbox{
  display: flex;
  justify-content: space-between;

  width: 100%;
  max-width: 90vw;
  height: 100vh;

  overflow: hidden;
  margin: 0 auto;
  padding: 15px;
}

.flexbox .board {
  display: flex;
  flex-direction: column;

  width: 100%;
  max-width: 20vw;

  background-color: #888;
  padding: 15px;
}

.flexbox .board .card {
  padding: 15px 25px;
  background-color: white;

  cursor: pointer;
  margin-bottom: 15px;
}
</style>
