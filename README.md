# Ajax Type-Ahead
Web app search tool that enables the user to search for city or state and view population. Features 'type-ahead' UI with results filtered by user input in real time. Built as part of 'JavaScript30' with Wes Bos.

Live demo: Coming soon

## Key Features
<ul>
  <li>A JSON file is stored in a variable 'endpoint' that contains a list of cities and their properties</li>
  <li>Using the JavaScript fetch API, the data is accessed, converted and stored in an array 'cities'.</li>
  <li>The search input and ul with class '.suggestions' are stored in variables.</li>
  <li>Event listeners are added to the search input that call the 'displayMatches' function on event change and keyup.</li>
  <li>The 'displayMatches' function calls 'findMatches' and stores the result in a variable 'matchArray'. findMatches filters through the cities array and matches against the value of the search input field to return any matches with the city or state (contained within the JSON).</li>
  <li>In 'displayMatches', another regex is created to replace the city and state with spans containing the matched search value, as well as append a class of '.hl' (for highlighting).</li>
  <li>'displayMatches' also returns HTML elements to display the city name, state name and population. In addition, the returning array is converted to one big string using 'join()' in order to format the HTML correctly.</li>
  <li>The HTML within '.suggestions' is then replaced with this newly updated HTML to display the search results dynamically.</li>
</ul>