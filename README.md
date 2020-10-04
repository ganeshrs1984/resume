# resume

var unirest = require("unirest");

var req = unirest("POST", "https://coinmarketcapzakutynskyv1.p.rapidapi.com/getCryptocurrenciesList");

req.headers({
	"x-rapidapi-host": "CoinMarketCapzakutynskyV1.p.rapidapi.com",
	"x-rapidapi-key": "894d74a8a1msh16255c013bae98cp12c159jsn94c6b7545007",
	"content-type": "application/x-www-form-urlencoded",
	"useQueryString": true
});

req.form({});

req.end(function (res) {
	if (res.error) throw new Error(res.error);

	console.log(res.body);
});
