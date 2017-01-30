# snek
simple snake game

z to turn left, x to turn right

<canvas width="320" height="320" id="canvas"></canvas>
<div>Score: <span id="score"></span></div>
<div id="gameOverMessage">
	The game is over. Press space to start another.
</div>
<hr/>


<script type="text/javascript" src="https://raw.githubusercontent.com/jmcd/snek/master/snek.js"></script>
<script type="text/javascript">

	document.addEventListener("DOMContentLoaded", function(event) { 
		
		var canvas = document.getElementById("canvas");

		var gameOverMessage = document.getElementById("gameOverMessage");
		var scoreElement = document.getElementById("score");

		addSnekGame(canvas, 0.05, {
			gameOverDidChange: function(gameOver) {
				gameOverMessage.hidden = !gameOver;
			},
			scoreDidChange: function(score) {
				scoreElement.innerHTML = score;
			}
		});

	});

</script>