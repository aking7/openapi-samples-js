<link rel="stylesheet" type="text/css" href="style.css">

<body>
    <h1>Instrument Search Demo</h1>
    <p>This sample demonstrates how to retrieve instruments via ad-hoc search through Saxo's OpenAPI.</p>
    <h2>Step 1: Grab an access token</h2>
    <p>Navigate to <a href="https://www.developer.saxo/openapi/token">Saxo's Developer Portal</a>, use your account to log in, and copy the 24-hour access token in the input field below:</p>
    <input type="text" class="text-input-field" id="tokenField" placeholder="Paste your token here..." />
    <input type="button" class="action-button" value="Verify token" id="checkTokenButton" />
    <br/>
    <pre id="userDataBlock">User information will appear here if token is valid...<br/><br/><br/></pre>
    <h2>Step 2: Retrieve list of accounts</h2>
    <p>Now that you are authenticated, the next step is to retrieve the account(s) that this user has access to. This information is required to obtain a list of instruments that are enabled (and searchable) for this client. A standard ('vanilla') demo client in SIM includes only a single test account.</p>
    <p>When the selection in the accounts dropdown is made (or changed), the list of legal asset types in Step 3 is automatically updated.</p>
    <input type="button" class="action-button" value="Get accounts" id="getAccountsButton" />
    <select class="selector" id="accountListSelector">
        <option value="" disabled selected>Your accounts will appear here...</option>
    </select>
    <h2>Step 3: Perform a search</h2>
    <p>Pick the type of instrument you would like to search for, enter a keyword and hit the search button to see the results. Up to 10 results will be displayed.</p>
    <select class="selector" id="assetTypeSelector">
        <option value="" disabled selected>Type...</option>
    </select>
    <input type="text" class="text-input-field" id="searchField" placeholder="Keyword..." />
    <input type="button" class="action-button" value="Search!" id="searchButton" />
    <br/>
    <pre id="searchResultBlock">Search results will appear here...</pre>
</body>

<script type="text/javascript" src="demo.js" defer></script>