# IO.Swagger - the C# library for the Tracko

No description provided (generated by Swagger Codegen https://github.com/swagger-api/swagger-codegen)

This C# SDK is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: v1
- SDK version: 1.0.0
- Build package: io.swagger.codegen.languages.CSharpClientCodegen

<a name="frameworks-supported"></a>
## Frameworks supported
- .NET 4.0 or later
- Windows Phone 7.1 (Mango)

<a name="dependencies"></a>
## Dependencies
- [RestSharp](https://www.nuget.org/packages/RestSharp) - 105.1.0 or later
- [Json.NET](https://www.nuget.org/packages/Newtonsoft.Json/) - 7.0.0 or later
- [JsonSubTypes](https://www.nuget.org/packages/JsonSubTypes/) - 1.2.0 or later

The DLLs included in the package may not be the latest version. We recommend using [NuGet](https://docs.nuget.org/consume/installing-nuget) to obtain the latest version of the packages:
```
Install-Package RestSharp
Install-Package Newtonsoft.Json
Install-Package JsonSubTypes
```

NOTE: RestSharp versions greater than 105.1.0 have a bug which causes file uploads to fail. See [RestSharp#742](https://github.com/restsharp/RestSharp/issues/742)

<a name="installation"></a>
## Installation
Run the following command to generate the DLL
- [Mac/Linux] `/bin/sh build.sh`
- [Windows] `build.bat`

Then include the DLL (under the `bin` folder) in the C# project, and use the namespaces:
```csharp
using IO.Swagger.trackoApiClient;
using IO.Swagger.Client;
using IO.Swagger.Model;
```
<a name="packaging"></a>
## Packaging

A `.nuspec` is included with the project. You can follow the Nuget quickstart to [create](https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package#create-the-package) and [publish](https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package#publish-the-package) packages.

This `.nuspec` uses placeholders from the `.csproj`, so build the `.csproj` directly:

```
nuget pack -Build -OutputDirectory out IO.Swagger.csproj
```

Then, publish to a [local feed](https://docs.microsoft.com/en-us/nuget/hosting-packages/local-feeds) or [other host](https://docs.microsoft.com/en-us/nuget/hosting-packages/overview) and consume the new package via Nuget as usual.

<a name="getting-started"></a>
## Getting Started

```csharp
using System;
using System.Diagnostics;
using IO.Swagger.trackoApiClient;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class Example
    {
        public void main()
        {

            var apiInstance = new AccettazioniApi();
            var oRequest = new BackofficeModelAccettazioniIndexMaskModel(); // BackofficeModelAccettazioniIndexMaskModel | 

            try
            {
                BackofficeModelAPICommonDataSourceResult result = apiInstance.AccettazioniGetList(oRequest);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling AccettazioniApi.AccettazioniGetList: " + e.Message );
            }

        }
    }
}
```

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to *https://areariservata.tracko.click*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AccettazioniApi* | [**AccettazioniGetList**](docs/AccettazioniApi.md#accettazionigetlist) | **POST** /api/Accettazioni/GetList | 
*AccettazioniStoricoApi* | [**AccettazioniStoricoGetList**](docs/AccettazioniStoricoApi.md#accettazionistoricogetlist) | **POST** /api/AccettazioniStorico/GetList | 
*ClientiApi* | [**ClientiGetList**](docs/ClientiApi.md#clientigetlist) | **POST** /api/Clienti/GetList | 
*ExternalMailerApi* | [**ExternalMailerHandlerMailup**](docs/ExternalMailerApi.md#externalmailerhandlermailup) | **POST** /api/ExternalMailer/HandlerMailup | 
*ExternalMailerApi* | [**ExternalMailerUpdateRequestStatus**](docs/ExternalMailerApi.md#externalmailerupdaterequeststatus) | **POST** /api/ExternalMailer/UpdateRequestStatus | 
*NewsletterApi* | [**NewsletterGetNewsletters**](docs/NewsletterApi.md#newslettergetnewsletters) | **POST** /api/Newsletter/GetNewsletters | 
*NewsletterApi* | [**NewsletterSaveNewsletters**](docs/NewsletterApi.md#newslettersavenewsletters) | **POST** /api/Newsletter/SaveNewsletters | 
*PermessiApi* | [**PermessiGetList**](docs/PermessiApi.md#permessigetlist) | **POST** /api/Permessi/GetList | 
*PermessiApi* | [**PermessiSavePermessi**](docs/PermessiApi.md#permessisavepermessi) | **POST** /api/Permessi/SavePermessi | 
*PolicyApi* | [**PolicyGetPolicy**](docs/PolicyApi.md#policygetpolicy) | **POST** /api/Policy/GetPolicy | 
*PolicyApi* | [**PolicySavePolicy**](docs/PolicyApi.md#policysavepolicy) | **POST** /api/Policy/SavePolicy | 
*SorgentiApi* | [**SorgentiGetList**](docs/SorgentiApi.md#sorgentigetlist) | **POST** /api/Sorgenti/GetList | 
*UtentiApi* | [**UtentiGetList**](docs/UtentiApi.md#utentigetlist) | **POST** /api/Utenti/GetList | 
*UtentiApi* | [**UtentiLockAccountCredential**](docs/UtentiApi.md#utentilockaccountcredential) | **POST** /api/Utenti/LockAccountCredential | 
*UtentiApi* | [**UtentiSendAccountCredential**](docs/UtentiApi.md#utentisendaccountcredential) | **POST** /api/Utenti/SendAccountCredential | 
*UtentiApi* | [**UtentiUnlockAccountCredential**](docs/UtentiApi.md#utentiunlockaccountcredential) | **POST** /api/Utenti/UnlockAccountCredential | 
*WSApi* | [**WSAddRequest**](docs/WSApi.md#wsaddrequest) | **POST** /api/WS/AddRequest | 
*WSApi* | [**WSGetPolicy**](docs/WSApi.md#wsgetpolicy) | **POST** /api/WS/GetPolicy | 
*WSApi* | [**WSGetUserAcceptance**](docs/WSApi.md#wsgetuseracceptance) | **POST** /api/WS/GetUserAcceptance | 
*WSApi* | [**WSRetrivePanelLink**](docs/WSApi.md#wsretrivepanellink) | **POST** /api/WS/RetrivePanelLink | 
*WSApi* | [**WSUpdateMultipleRequestStatus**](docs/WSApi.md#wsupdatemultiplerequeststatus) | **POST** /api/WS/UpdateMultipleRequestStatus | 
*WSApi* | [**WSUpdateRequestStatus**](docs/WSApi.md#wsupdaterequeststatus) | **POST** /api/WS/UpdateRequestStatus | 


<a name="documentation-for-models"></a>
## Documentation for Models

 - [Model.BackofficeModelAPICommonDataSourceResult](docs/BackofficeModelAPICommonDataSourceResult.md)
 - [Model.BackofficeModelAPICommonMessageModel](docs/BackofficeModelAPICommonMessageModel.md)
 - [Model.BackofficeModelAPINewsletterGetNewslettersRequestData](docs/BackofficeModelAPINewsletterGetNewslettersRequestData.md)
 - [Model.BackofficeModelAPINewsletterGetNewslettersResponseData](docs/BackofficeModelAPINewsletterGetNewslettersResponseData.md)
 - [Model.BackofficeModelAPINewsletterSaveNewsletterRequestData](docs/BackofficeModelAPINewsletterSaveNewsletterRequestData.md)
 - [Model.BackofficeModelAPINewsletterSaveNewsletterRequestItem](docs/BackofficeModelAPINewsletterSaveNewsletterRequestItem.md)
 - [Model.BackofficeModelAPINewsletterSaveNewsletterResponseData](docs/BackofficeModelAPINewsletterSaveNewsletterResponseData.md)
 - [Model.BackofficeModelAPIPermessiGetListRequestData](docs/BackofficeModelAPIPermessiGetListRequestData.md)
 - [Model.BackofficeModelAPIPermessiGetListResponseData](docs/BackofficeModelAPIPermessiGetListResponseData.md)
 - [Model.BackofficeModelAPIPermessiGetListResponseDataItem](docs/BackofficeModelAPIPermessiGetListResponseDataItem.md)
 - [Model.BackofficeModelAPIPermessiSaveRequestData](docs/BackofficeModelAPIPermessiSaveRequestData.md)
 - [Model.BackofficeModelAPIPermessiSaveRequestDataItem](docs/BackofficeModelAPIPermessiSaveRequestDataItem.md)
 - [Model.BackofficeModelAPIPolicyGetPolicyRequestData](docs/BackofficeModelAPIPolicyGetPolicyRequestData.md)
 - [Model.BackofficeModelAPIPolicyGetPolicyResponseData](docs/BackofficeModelAPIPolicyGetPolicyResponseData.md)
 - [Model.BackofficeModelAPIPolicySavePolicyRequestData](docs/BackofficeModelAPIPolicySavePolicyRequestData.md)
 - [Model.BackofficeModelAPIWSContactAddRequestAccettazioniData](docs/BackofficeModelAPIWSContactAddRequestAccettazioniData.md)
 - [Model.BackofficeModelAPIWSContactAddRequestAccettazioniDataItem](docs/BackofficeModelAPIWSContactAddRequestAccettazioniDataItem.md)
 - [Model.BackofficeModelAPIWSContactAddRequestRequestData](docs/BackofficeModelAPIWSContactAddRequestRequestData.md)
 - [Model.BackofficeModelAPIWSContactAddRequestResponseData](docs/BackofficeModelAPIWSContactAddRequestResponseData.md)
 - [Model.BackofficeModelAPIWSContactAddRequestRichiestaData](docs/BackofficeModelAPIWSContactAddRequestRichiestaData.md)
 - [Model.BackofficeModelAPIWSContactAddRequestRichiestaDataItem](docs/BackofficeModelAPIWSContactAddRequestRichiestaDataItem.md)
 - [Model.BackofficeModelAPIWSContactAddRequestSearchIdDataItem](docs/BackofficeModelAPIWSContactAddRequestSearchIdDataItem.md)
 - [Model.BackofficeModelAPIWSContactAddRequestSearchIdsData](docs/BackofficeModelAPIWSContactAddRequestSearchIdsData.md)
 - [Model.BackofficeModelAPIWSContactGetUserAcceptanceRequestData](docs/BackofficeModelAPIWSContactGetUserAcceptanceRequestData.md)
 - [Model.BackofficeModelAPIWSContactGetUserAcceptanceResponseData](docs/BackofficeModelAPIWSContactGetUserAcceptanceResponseData.md)
 - [Model.BackofficeModelAPIWSContactRetrivePanelLinkRequestData](docs/BackofficeModelAPIWSContactRetrivePanelLinkRequestData.md)
 - [Model.BackofficeModelAPIWSContactRetrivePanelLinkResponseData](docs/BackofficeModelAPIWSContactRetrivePanelLinkResponseData.md)
 - [Model.BackofficeModelAPIWSContactUpdateMultipleRequestStatusRequestData](docs/BackofficeModelAPIWSContactUpdateMultipleRequestStatusRequestData.md)
 - [Model.BackofficeModelAPIWSContactUpdateMultipleRequestStatusRequestDataItem](docs/BackofficeModelAPIWSContactUpdateMultipleRequestStatusRequestDataItem.md)
 - [Model.BackofficeModelAPIWSContactUpdateMultipleRequestStatusResponseData](docs/BackofficeModelAPIWSContactUpdateMultipleRequestStatusResponseData.md)
 - [Model.BackofficeModelAPIWSContactUpdateRequestStatusRequestData](docs/BackofficeModelAPIWSContactUpdateRequestStatusRequestData.md)
 - [Model.BackofficeModelAPIWSContactUpdateRequestStatusRequestDataItem](docs/BackofficeModelAPIWSContactUpdateRequestStatusRequestDataItem.md)
 - [Model.BackofficeModelAPIWSContactUpdateRequestStatusResponseData](docs/BackofficeModelAPIWSContactUpdateRequestStatusResponseData.md)
 - [Model.BackofficeModelAPIWSPolicyGetPolicyRequestData](docs/BackofficeModelAPIWSPolicyGetPolicyRequestData.md)
 - [Model.BackofficeModelAPIWSPolicyGetPolicyResponseData](docs/BackofficeModelAPIWSPolicyGetPolicyResponseData.md)
 - [Model.BackofficeModelAccettazioniIndexMaskModel](docs/BackofficeModelAccettazioniIndexMaskModel.md)
 - [Model.BackofficeModelSorgentiIndexMaskModel](docs/BackofficeModelSorgentiIndexMaskModel.md)
 - [Model.BackofficeModelWSAPIHooksHandlerMailupData](docs/BackofficeModelWSAPIHooksHandlerMailupData.md)
 - [Model.ModelLayerBackDatatableResponseAccettazioniStoricoDtAjaxPost](docs/ModelLayerBackDatatableResponseAccettazioniStoricoDtAjaxPost.md)
 - [Model.ModelLayerBackDatatableResponseColumn](docs/ModelLayerBackDatatableResponseColumn.md)
 - [Model.ModelLayerBackDatatableResponseOrder](docs/ModelLayerBackDatatableResponseOrder.md)
 - [Model.ModelLayerBackDatatableResponseSearch](docs/ModelLayerBackDatatableResponseSearch.md)
 - [Model.ModelLayerNewsletterMailUpExportParameter](docs/ModelLayerNewsletterMailUpExportParameter.md)
 - [Model.ModelLayerNewsletterMailUpSearchParameter](docs/ModelLayerNewsletterMailUpSearchParameter.md)


<a name="documentation-for-authorization"></a>
## Documentation for Authorization

All endpoints do not require authorization.
