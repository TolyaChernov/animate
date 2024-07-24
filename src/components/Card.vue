<template>
  <div class="card-container ml-10 mt-10">
    <div class="card">
      <div class="front rounded-lg p-5">Front of the Card</div>
      <div class="back rounded-lg p-5">Back of the Card</div>
    </div>
  </div>
</template>

<style>
.card-container {
  perspective: 2000px;
}

.card {
  width: 294px;
  height: 290px;
  transition: transform 2s;
  transform-style: preserve-3d;
}

.card:hover {
  transform: rotateY(180deg);
}

.front,
.back {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
}

.front {
  background-color: #26cf10;
}

.back {
  background-color: #4c7fec;
  transform: rotateY(180deg);
}
</style>
