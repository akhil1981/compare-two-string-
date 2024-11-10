<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>String Comparison</title>

</head>

<body>

<h1>String Comparison</h1>

<div class="form-section">

<label for="string1">Enter First String: </label>

<input type="text" id="string1" placeholder="Enter first string">

<br><br>

<label for="string2">Enter Second String: </label>

<input type="text" id="string2" placeholder="Enter second string">

<br><br>

<button onclick="compareStrings()">Compare Strings</button>

</div>

<div id="comparisonResult"></div>

<script> function compareStrings() {

const str1 = document.getElementById('string1').value;

const str2 = document.getElementById('string2').value;

let result = '';

if (str1 === str2) {

result += `<p>Strings are exactly the same (case-sensitive comparison).</p>`;

} else {

result += `<p>Strings are NOT the same (case-sensitive comparison).</p>`;

}

if (str1.toLowerCase() === str2.toLowerCase()) {

result += `<p>Strings are the same (case-insensitive comparison).</p>`;

} else {

result += `<p>Strings are NOT the same (case-insensitive comparison).</p>`;

}

if (str1.includes(str2)) {

result += `<p>First string includes the second string.</p>`;

} else if (str2.includes(str1)) {

result += `<p>Second string includes the first string.</p>`;

} else {

result += `<p>Neither string includes the other.</p>`;

}

if (str1.length === str2.length) {

result += `<p>Both strings have the same length.</p>`;

} else if (str1.length > str2.length) {

result += `<p>First string is longer than the second string.</p>`;

} else {

result += `<p>Second string is longer than the first string.</p>`;

}

if (str1 < str2) {

result += `<p>First string comes before the second string lexicographically.</p>`;

} else if (str1 > str2) {

result += `<p>Second string comes before the first string lexicographically.</p>`;

} else {

result += `<p>Both strings are lexicographically equal.</p>`;

}

document.getElementById('comparisonResult').innerHTML = result;

}

</script>

</body>

</html>
