# ![LOGO](logo.png) Real-Time Rail Predictions **flow**ground Connector

## Description

A generated **flow**ground connector for the Real-Time Rail Predictions API (version 1.0).

Generated from: https://api.apis.guru/v2/specs/wmata.com/rail-realtime/1.0/swagger.json<br/>
Generated at: 2019-05-07T17:44:59+03:00

## API Description

Real-time rail prediction methods.

## Authorization

Supported authorization schemes:
- API Key- API Key
## Actions

### XML - Next Trains

> <h4 class="text-primary">Description</h4><br/>
> <br/>
> <p>Returns next train arrival information for one or more stations. Will return<br/>
> an empty set of results when no predictions are available. Use <span class=<br/>
> "text-info">All</span> for the StationCodes parameter to return predictions for<br/>
> all stations.</p><br/>
> <br/>
> <p>For terminal stations (e.g.: Greenbelt, Shady Grove, etc.), predictions may<br/>
> be displayed twice.</p><br/>
> <br/>
> <p>Some stations have two platforms (e.g.: Gallery Place, Fort Totten, L'Enfant<br/>
> Plaza, and Metro Center). To retrieve complete predictions for these stations,<br/>
> be sure to pass in both StationCodes.</p><br/>
> <br/>
> <p>For trains with no passengers, the DestinationName will be <span class=<br/>
> "text-info">No Passenger</span>.</p><br/>
> <br/>
> <p>Next train arrival information is refreshed once every 20 to 30 seconds approximately.</p><br/>
> <br/>
> <h4 class="text-primary">Response Elements</h4><br/>
> <br/>
> <table class="table table-condensed table-hover"><br/>
> <thead><br/>
> <tr><br/>
> <th class="col-md-3">Element</th><br/>
> <br/>
> <th>Description</th><br/>
> </tr><br/>
> </thead><br/>
> <br/>
> <tbody><br/>
> <tr><br/>
> <td>Trains</td><br/>
> <br/>
> <td><br/>
> Array containing train prediction information (<a href=<br/>
> "#AIMPredictionTrainInfo">AIMPredictionTrainInfo</a>).<br/>
> </td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td colspan="2"><br/>
> <div class="text-primary" style="margin-top: 1em"><br/>
> <a id="AIMPredictionTrainInfo" name=<br/>
> "AIMPredictionTrainInfo">AIMPredictionTrainInfo<br/>
> Elements</a><br/>
> </div><br/>
> </td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>Car</td><br/>
> <br/>
> <td>Number of cars on a train, usually 6 or 8, but might also<br/>
> return <span class="text-info">-</span> or NULL.</td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>Destination</td><br/>
> <br/>
> <td>Abbreviated version of the final destination for a train. This<br/>
> is similar to what is displayed on the signs at stations.</td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>DestinationCode</td><br/>
> <br/>
> <td>Destination station code. Can be NULL. Use this value in other<br/>
> rail-related APIs to retrieve data about a station.</td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>DestinationName</td><br/>
> <br/>
> <td>When DestinationCode is populated, this is the full name of the<br/>
> destination station, as shown on the WMATA website.</td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>Group</td><br/>
> <br/>
> <td>Denotes the track this train is on, but does not necessarily<br/>
> equate to Track 1 or Track 2. With the exception of terminal<br/>
> stations, predictions at the same station with different Group<br/>
> values refer to trains on different tracks.</td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>Line</td><br/>
> <br/>
> <td>Two-letter abbreviation for the line (e.g.: RD, BL, YL, OR, GR,<br/>
> or SV). May also be blank or <span class="text-info">No</span> for<br/>
> trains with no passengers.</td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>LocationCode</td><br/>
> <br/>
> <td>Station code for where the train is arriving. Useful when<br/>
> passing in <span class="text-info">All</span> as the StationCodes<br/>
> parameter. Use this value in other rail-related APIs to retrieve<br/>
> data about a station.</td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>LocationName</td><br/>
> <br/>
> <td>Full name of the station where the train is arriving. Useful<br/>
> when passing in <span class="text-info">All</span> as the<br/>
> StationCodes parameter.</td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>Min</td><br/>
> <br/>
> <td>Minutes until arrival. Can be a numeric value, <span class=<br/>
> "text-info">ARR</span> (arriving), <span class=<br/>
> "text-info">BRD</span> (boarding), <span class=<br/>
> "text-info">---</span>, or empty.</td><br/>
> </tr><br/>
> </tbody><br/>
> </table><br/>
> <hr>

#### Input Parameters
* `StationCodes` - _required_ - Comma-separated list of station codes.  For all predictions, use "All".
    Possible values: B03, All.

### JSON - Next Trains

> <h4 class="text-primary">Description</h4><br/>
> <br/>
> <p>Returns next train arrival information for one or more stations. Will return<br/>
> an empty set of results when no predictions are available. Use <span class=<br/>
> "text-info">All</span> for the StationCodes parameter to return predictions for<br/>
> all stations.</p><br/>
> <br/>
> <p>For terminal stations (e.g.: Greenbelt, Shady Grove, etc.), predictions may<br/>
> be displayed twice.</p><br/>
> <br/>
> <p>Some stations have two platforms (e.g.: Gallery Place, Fort Totten, L'Enfant<br/>
> Plaza, and Metro Center). To retrieve complete predictions for these stations,<br/>
> be sure to pass in both StationCodes.</p><br/>
> <br/>
> <p>For trains with no passengers, the DestinationName will be <span class=<br/>
> "text-info">No Passenger</span>.</p><br/>
> <br/>
> <p>Next train arrival information is refreshed once every 20 to 30 seconds approximately.</p><br/>
> <br/>
> <h4 class="text-primary">Response Elements</h4><br/>
> <br/>
> <table class="table table-condensed table-hover"><br/>
> <thead><br/>
> <tr><br/>
> <th class="col-md-3">Element</th><br/>
> <br/>
> <th>Description</th><br/>
> </tr><br/>
> </thead><br/>
> <br/>
> <tbody><br/>
> <tr><br/>
> <td>Trains</td><br/>
> <br/>
> <td><br/>
> Array containing train prediction information (<a href=<br/>
> "#AIMPredictionTrainInfo">AIMPredictionTrainInfo</a>).<br/>
> </td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td colspan="2"><br/>
> <div class="text-primary" style="margin-top: 1em"><br/>
> <a id="AIMPredictionTrainInfo" name=<br/>
> "AIMPredictionTrainInfo">AIMPredictionTrainInfo<br/>
> Elements</a><br/>
> </div><br/>
> </td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>Car</td><br/>
> <br/>
> <td>Number of cars on a train, usually 6 or 8, but might also<br/>
> return <span class="text-info">-</span> or NULL.</td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>Destination</td><br/>
> <br/>
> <td>Abbreviated version of the final destination for a train. This<br/>
> is similar to what is displayed on the signs at stations.</td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>DestinationCode</td><br/>
> <br/>
> <td>Destination station code. Can be NULL. Use this value in other<br/>
> rail-related APIs to retrieve data about a station.</td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>DestinationName</td><br/>
> <br/>
> <td>When DestinationCode is populated, this is the full name of the<br/>
> destination station, as shown on the WMATA website.</td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>Group</td><br/>
> <br/>
> <td>Denotes the track this train is on, but does not necessarily<br/>
> equate to Track 1 or Track 2. With the exception of terminal<br/>
> stations, predictions at the same station with different Group<br/>
> values refer to trains on different tracks.</td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>Line</td><br/>
> <br/>
> <td>Two-letter abbreviation for the line (e.g.: RD, BL, YL, OR, GR,<br/>
> or SV). May also be blank or <span class="text-info">No</span> for<br/>
> trains with no passengers.</td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>LocationCode</td><br/>
> <br/>
> <td>Station code for where the train is arriving. Useful when<br/>
> passing in <span class="text-info">All</span> as the StationCodes<br/>
> parameter. Use this value in other rail-related APIs to retrieve<br/>
> data about a station.</td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>LocationName</td><br/>
> <br/>
> <td>Full name of the station where the train is arriving. Useful<br/>
> when passing in <span class="text-info">All</span> as the<br/>
> StationCodes parameter.</td><br/>
> </tr><br/>
> <br/>
> <tr><br/>
> <td>Min</td><br/>
> <br/>
> <td>Minutes until arrival. Can be a numeric value, <span class=<br/>
> "text-info">ARR</span> (arriving), <span class=<br/>
> "text-info">BRD</span> (boarding), <span class=<br/>
> "text-info">---</span>, or empty.</td><br/>
> </tr><br/>
> </tbody><br/>
> </table><br/>
> <hr>

#### Input Parameters
* `StationCodes` - _required_ - Comma-separated list of station codes.  For all predictions, use "All".
    Possible values: B03, All.

## License

**flow**ground :- Telekom iPaaS / wmata-com-rail-realtime-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
