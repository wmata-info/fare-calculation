# DC Metro API Documentation

## Overview

The DC Metro API, hosted at `api.dcmet.ro`, offers a streamlined and efficient way to access real-time transit data. Built on FastAPI and SQLite3, this API integrates seamlessly with WMATA data, ensuring accuracy and timeliness. We aim to provide a user-friendly, accessible experience for developers and end-users alike.

### Features

- **Direct Integration**: Data sourced from WMATA.
- **Accessibility**: Available at `api.dcmet.ro` and via our GitHub repository (link to be provided).
- **Fast Responses**: Local hosting delivers results within approximately 5ms.
- **Format**: Exclusively supports JSON data.
- **Customizable**: User-friendly design for custom data structures.
- **Security**: When you send a request to `api.dcmet.ro`, both your requests and the response are **always** encrypted from end-to-end.
- **Compatibility**: Matches WMATA's default data format for easy integration.
- **Cost-Effective**: Free access, with optional paid consultations.

### Data Structure and Sample Responses

Structured data samples are provided based on the request URL, allowing users to customize the API's output according to their needs.

#### Sample Response

```json
{
  "StationToStationInfos": [
    {
      "SourceStation": "C11",
      "DestinationStation": "J03",
      "CompositeMiles": 8.73,
      "RailTime": 15,
      "RailFare": {
        "PeakTime": 4.3,
        "OffPeakTime": 3.3,
        "SeniorDisabled": 2.15
      }
    }
  ]
}
```

### Request Parameters

#### Optional Parameters

1. **FromStationCode** (string): Specifies the code for the origin station. 

2. **ToStationCode** (string): Specifies the code for the destination station.


Both of the above parameters are verified by the following regex: 
```bash
^[ABCDEFGHJKN]\d{2}$
```

**Note**: Omitting both `FromStationCode` and `ToStationCode` will result in the API returning the entire database.

### User Customization

The API's design is intuitive and easily modifiable to accommodate different data structures.

### Implementation and Support

- **User-Friendly**: Detailed documentation supports a straightforward implementation process.
- **Feedback and Reviews**: Your experiences and reviews are invaluable to us.
- **Consultation Services**: Expert consultations are available for more intricate requirements.
- **Community Engagement**: Aimed at extending service to all of WMATA's static APIs.

### No API Key Required

Our commitment to accessibility extends to a no-API-key-required policy, simplifying the integration process.

---

*Reminder: This API is provided free of charge. Your feedback and reviews are crucial in helping us improve and serve the community more effectively.*

***We cannot guarentee uptime right now for `api.dcmet.ro`, for guaranteed uptime download our repostiory when available***
