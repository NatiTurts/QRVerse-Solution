# QRVerse

Create Dynamic QR Codes Directly in Power Platform

-----------
## Purpose
QRVerse Pro is a powerful connector that allows you to generate various types of QR codes within Power Automate and Power Apps. By integrating with an Azure Function via RapidAPI, you can create WiFi, vCard, location, event, and URL QR codes effortlessly.


## Features

- Generate WiFi QR Codes: Share network credentials securely.
- Create vCard QR Codes: Provide contact information with a scan.
- Produce Location QR Codes: Share precise geographic locations.
- Schedule Event QR Codes: Send event details seamlessly.
- Generate URL QR Codes: Direct users to websites instantly.


## How to Configure and Use
### Obtain API Key
1. Visit RapidAPI [here](https://rapidapi.com/turtledovecloudsolutions12-turtledovecloudsolutions-default/api/qrverse3/pricing)
2. Subscribe to a plan
3. Obtain your unique API key upon subcription

## Set Up in Power Platform - HTTP Request
1. Create a new flow or app
2. Add the HTTP action to make the API call
3. Set the request method to POST
4. Use the appropriate endpoint (below)
5. Include your API Key in the headers:
```
"Content-Type": "application/json",
"x-rapidapi-host": "qrverse3.p.rapidapi.com",
"x-rapidapi-key": "YOUR_API_KEY" 
```
6. Construct the JSON body according to the schema of the QR code you wish to generate.

## Set Up in Power Platform - Custom Connector
1. Create a new flow or app
2. Add the QrVerse Custom Connector
3. Initiate a new connection reference using your API Key
4. Fill in the input parameters for the action
5. Compose the response output for the selected action


## API Endpoints and Schemas
**Generate WiFi QR Code**

- Endpoint: `https://qrverse3.p.rapidapi.com/generate/wifi`
- Schema: 
```
{
  "ssid": "MyNetwork",
  "password": "SecurePassword",
  "authType": "WPA",
  "qrColor": "#008000",
  "backgroundColor": "#FFFFFF"
}
```
- Response: 
```
{
  "qrCodeSvg": "SVGCode"
}
```

**Generate vCard QR Code**

- Endpoint: `https://qrverse3.p.rapidapi.com/generate/vcard`
- Schema: 
```
{
  "firstName": "John",
  "middleName": "A.",
  "lastName": "Doe",
  "company": "Example Corp",
  "jobTitle": "Software Engineer",
  "phoneWork": "+1234567890",
  "phoneMobile": "+0987654321",
  "email": "john.doe@example.com",
  "website": "https://www.example.com",
  "address1": "123 Main St",
  "address2": "Suite 100",
  "city": "Anytown",
  "postcode": "12345",
  "country": "USA",
  "qrColor": "#0000FF",
  "backgroundColor": "#00FFFF"
}
```
- Response: 
```
{
  "qrCodeSvg": "SVGCode"
}
```

**Generate Location QR Code**

- Endpoint: `https://qrverse3.p.rapidapi.com/generate/location`
- Schema: 
```
{
  "latitude": "37.7749",
  "longitude": "-122.4194",
  "qrColor": "#800080",
  "backgroundColor": "#FFC0CB"
}
```
- Response: 
```
{
  "qrCodeSvg": "SVGCode"
}
```


**Generate Event QR Code**

- Endpoint: `https://qrverse3.p.rapidapi.com/generate/event`
- Schema: 
```
{
  "summary": "Project Meeting",
  "location": "Conference Room 1",
  "startDate": "2023-11-01",
  "startTime": "10:00",
  "endDate": "2023-11-01",
  "endTime": "11:30",
  "qrColor": "#FFA500",
  "backgroundColor": "#FFFFFF"
}
```
- Response: 
```
{
  "qrCodeSvg": "SVGCode"
}
```


**Generate URL QR Code**

- Endpoint: `https://qrverse3.p.rapidapi.com/generate/url`
- Schema: 
```
{
  "url": "https://www.nati-turtledove.com",
  "qrColor": "#FF5733",
  "backgroundColor": "#C0C0C0"
}
```
- Response: 
```
{
  "qrCodeSvg": "SVGCode"
}
```


## Costing
- Basic: $0.00/month for up to 10 API calls.
- Pro: $5.00/month for up to 500 API calls
- Ultra: $15.00/month for up to 1,000 API calls
- Mega: Unlimited calls at $0.004/call

## Support
For assistance, please visit our Support Center or contact us at support@turtledovecloudsolutions.com.
