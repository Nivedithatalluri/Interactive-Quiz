# Interactive-Quiz
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Quiz</title>
    <script>
        // Function to calculate the score
        function calculateScore() {
            var score = 0;

  // Check for answers using getElementsByName
            var q0 = document.getElementsByName("q0");
            for (var i = 0; i < q0.length; i++) {
                if (q0[i].checked && q0[i].value === '0') {
                    score++;
                }
            }
var q1 = document.getElementsByName("q1");
            for (var i = 0; i < q1.length; i++) {
                if (q1[i].checked && q1[i].value === '1') {
                    score++;
                }
            }
var q2 = document.getElementsByName("q2");
            for (var i = 0; i < q2.length; i++) {
                if (q2[i].checked && q2[i].value === '2') {
                    score++;
                }
            }

 // Display the score
            document.getElementById("result").innerHTML = "Your score: " + score + " / 3";
        }
    </script>
</head>
<body>

<h2>Interactive Quiz</h2>

<form id="quizForm">
        <p><b>1. What is the capital of France?</b></p>
        <input type="radio" name="q0" value="0"> Paris <br>
        <input type="radio" name="q0" value="1"> London <br>
        <input type="radio" name="q0" value="2"> Berlin <br>
        <input type="radio" name="q0" value="3"> Madrid <br><br>

  <p><b>2. Which planet is known as the Red Planet?</b></p>
        <input type="radio" name="q1" value="0"> Earth <br>
        <input type="radio" name="q1" value="1"> Mars <br>
        <input type="radio" name="q1" value="2"> Jupiter <br>
        <input type="radio" name="q1" value="3"> Saturn <br><br>

  <p><b>3. What is the largest ocean on Earth?</b></p>
        <input type="radio" name="q2" value="0"> Atlantic <br>
        <input type="radio" name="q2" value="1"> Indian <br>
        <input type="radio" name="q2" value="2"> Pacific <br>
        <input type="radio" name="q2" value="3"> Arctic <br><br>

  <button type="button" onclick="calculateScore()">Submit Answers</button>
    </form>

  <p id="result"></p>

</body>
</html>
