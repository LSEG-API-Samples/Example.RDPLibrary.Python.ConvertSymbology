# Example.RDPLibrary.Python.ConvertSymbology
## Symbology Conversion Example
This is a simple notebook I created for a customer, demonstrating how to convert ISINs (or other Symbology) to RICs using the Refinitiv Data Platform Symbology API.
Whilst, I will be working with ISINs and RICs, the API supports other types such as:
- RIC
- ISIN
- CUSIP
- SEDOL
- LEI (Legal Entity Identifier)
- PermID
- others...

Note that whilst the Symbology API is quiet flexible, it may not always be possible to convert a symbol from one type to another - based on the to/from type combination and asset class involved etc.

Please refer to the following, for further details:
- [Symbology API Reference](https://apidocs.refinitiv.com/Apps/ApiDocs#/details/L2Rpc2NvdmVyeS9zeW1ib2xvZ3kvdjE=/L2xvb2t1cA==/POST/README) - in particular, the section *'identifier types covered by asset class'*
- [Symbology API User Guide](https://developers.refinitiv.com/en/api-catalog/refinitiv-data-platform/refinitiv-data-platform-apis/documentation#symbology-user-guide)

I will be using the [RDP Python Library](https://developers.refinitiv.com/en/api-catalog/refinitiv-data-platform/refinitiv-data-platform-libraries) to keep things simple. The RDP Library is a ease of wrapper for the RDP APIs and is available in Python, .NET and soon in Typescript.

However, if you are not using one of the above languages, you can still access the Symbology API and the other RDP APIs via a HTTP RESTful interface - as [detailed here](https://developers.refinitiv.com/en/api-catalog/refinitiv-data-platform/refinitiv-data-platform-apis/tutorials#introduction-to-the-request-response-api)

### Access Credentials
For details on Access Credentials, please see the [RDP Library Quick Start](https://developers.refinitiv.com/en/api-catalog/refinitiv-data-platform/refinitiv-data-platform-libraries/quick-start)

## NOTE: Whilst the RDP Library has built in conver_symbol() functions, this call actually uses the RDP Search API - which you requires different licencing.
