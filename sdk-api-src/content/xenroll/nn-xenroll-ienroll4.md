---
UID: NN:xenroll.IEnroll4
title: IEnroll4
author: windows-driver-content
description: The IEnroll4 interface represents the Certificate Enrollment Control and is used primarily to generate certificate requests.
old-location: security\ienroll4.htm
old-project: SecCrypto
ms.assetid: 133529fb-e02a-41a2-83df-646cbc01dbe9
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IEnroll4, IEnroll4 interface [Security], IEnroll4 interface [Security],described, security.ienroll4, xenroll/IEnroll4
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Xenroll.dll
api_name:
-	IEnroll4
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll4 interface


## -description


<p class="CCE_Message">[This interface is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>IEnroll4</b> interface represents the Certificate Enrollment Control and is used primarily to generate <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate requests</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnroll4</b> interface inherits from <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> and <a href="https://msdn.microsoft.com/60a28944-35de-4ea2-8523-5634685ac224">IEnroll2</a>. <b>IEnroll4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IEnroll4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c2b99df-769b-457b-b5c5-7690b73d6f84">acceptFilePKCS7WStr</a>
</td>
<td align="left" width="63%">
Accepts and processes a PKCS #7 message containing a certificate, then stores the message to a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9c92f20-5f23-4dda-9e80-df9bf400ac08">acceptFileResponseWStr</a>
</td>
<td align="left" width="63%">
Accepts delivery of the credentials issued in response to an earlier call to 
<a href="https://msdn.microsoft.com/5750f2ad-a96f-4bc7-9a1f-354e279a7860">createFileRequestWStr</a>, and it places the credentials in the appropriate store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8772f528-2c33-48f4-bb0c-cfde91cf2fba">acceptPKCS7Blob</a>
</td>
<td align="left" width="63%">
Accepts and processes a PKCS #7 message containing a certificate. The PKCS #7 is input as a parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a28bf6b-ad3d-414b-8740-ce7d4301a05b">acceptResponseBlob</a>
</td>
<td align="left" width="63%">
Accepts delivery of the credentials issued in response to an earlier call to 
<a href="https://msdn.microsoft.com/bc2b875c-96f8-453e-8f72-f9032d5aa773">createRequestWStr</a> and places the credentials in the appropriate store. 
				

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71421bca-ef72-47d3-8f4a-95cb9768644f">addAttributeToRequestWStr</a>
</td>
<td align="left" width="63%">
Adds an attribute to the certificate request.
			 



				

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a65eca3d-8308-4bdc-b851-016a4e63a1f1">AddAuthenticatedAttributesToPKCS7Request</a>
</td>
<td align="left" width="63%">
Adds authenticated attributes to a PKCS #7 certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/954c1b2f-08ea-471c-902f-1aa5523d58b3">addBlobPropertyToCertificateWStr</a>
</td>
<td align="left" width="63%">
Adds a BLOB property to a certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9bf51db-375e-4230-953c-d9893228d7e1">AddCertTypeToRequestWStr</a>
</td>
<td align="left" width="63%">
Adds a certificate template to a request (used to support the enterprise <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA)).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa3bab0d-2ed4-4ef2-9665-a6c70e14308d">AddCertTypeToRequestWStrEx</a>
</td>
<td align="left" width="63%">
Adds a certificate template (or "certificate type") to a request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6976fd52-98f0-4eff-aa83-7cf5cb5d5e67">AddExtensionsToRequest</a>
</td>
<td align="left" width="63%">
Adds extensions to the certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ecca64b-a8f4-4816-8bf1-7b8e74262ac0">addExtensionToRequestWStr</a>
</td>
<td align="left" width="63%">
Adds an extension to the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25f8ae01-e975-4ada-b17c-c97385dc0585">addNameValuePairToRequestWStr</a>
</td>
<td align="left" width="63%">
Adds a name-value string pair to the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ccc0bdf-01db-4863-aaaf-94910bfa0b8b">AddNameValuePairToSignatureWStr</a>
</td>
<td align="left" width="63%">
Adds the name and value pair of an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a> to the request. It is up to the CA to interpret the meaning of the name-value pair.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ce10b31-29f4-4fda-a488-7bc124e9461e">binaryBlobToString</a>
</td>
<td align="left" width="63%">
Converts a binary data BLOB to a string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1df364e7-35ab-4c16-ac13-2f0be36fe0f9">createFilePFXWStr</a>
</td>
<td align="left" width="63%">
Saves the accepted certificate chain and private key in a file in PFX format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5edd54c5-9dfb-44b8-a293-4fe6a8de45e3">createFilePKCS10WStr</a>
</td>
<td align="left" width="63%">
Creates a base64-encoded PKCS #10 <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a> and saves it in a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5750f2ad-a96f-4bc7-9a1f-354e279a7860">createFileRequestWStr</a>
</td>
<td align="left" width="63%">
Creates a PKCS #10 certificate request, a PKCS #7 request, or a Full CMC certificate request and stores it in a file.
			 



				

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38ab5b07-2a84-484b-b413-58f0e11599e9">createPFXWStr</a>
</td>
<td align="left" width="63%">
Saves the accepted certificate chain and private key in a Personal Information Exchange (PFX) format string. The PFX format is also known as PKCS #12.
			
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebbcc9ad-9f87-4abe-963b-38c57a60e45e">createPKCS10WStr</a>
</td>
<td align="left" width="63%">
Creates a base64-encoded PKCS #10 certificate request.
			

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1d2df72-bedc-45e5-8c0a-a731845d4487">CreatePKCS7RequestFromRequest</a>
</td>
<td align="left" width="63%">
Creates a PKCS #7 request from an existing certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc2b875c-96f8-453e-8f72-f9032d5aa773">createRequestWStr</a>
</td>
<td align="left" width="63%">
Creates a PKCS #10, PKCS #7, or Full CMC format certificate request and stores it in a string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a40d85d0-fd02-4e0a-af7d-dfefe02f4e2a">EnumAlgs</a>
</td>
<td align="left" width="63%">
Retrieves the IDs of cryptographic algorithms in a given algorithm class that are supported by the current CSP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a08d97c9-8ee9-464e-862e-18c335695927">enumContainersWStr</a>
</td>
<td align="left" width="63%">
Retrieves the names of the containers for the CSP specified by the 
<a href="https://msdn.microsoft.com/42300501-2a64-4433-81e9-6ee3fc31b094">ProviderNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae1ac12c-0332-4796-8269-a3b6f72b8bff">enumPendingRequestWStr</a>
</td>
<td align="left" width="63%">
Enumerates pending certificate requests and retrieves a specified property from each.
			
		
				

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3b40f56-3332-44e8-9753-4107948d0801">enumProvidersWStr</a>
</td>
<td align="left" width="63%">
Retrieves the names of the available <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service providers</a> (CSPs) specified by the 
<a href="https://msdn.microsoft.com/d4ab2b0e-127f-4ec0-9e4a-4314561912e3">ProviderType</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c89de98-51b6-44c2-acd2-879d1d4e7f29">freeRequestInfoBlob</a>
</td>
<td align="left" width="63%">
Deletes a certificate context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/294a8a38-9c76-4e5c-ac11-2fcb8b81727e">get_CAStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/294a8a38-9c76-4e5c-ac11-2fcb8b81727e">CAStoreFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c016649-a780-45c1-94a4-fb08c15c4e0f">get_CAStoreNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/4c016649-a780-45c1-94a4-fb08c15c4e0f">CAStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbb60c1c-04ed-4477-bf8e-4dae9fd964ef">get_CAStoreTypeWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/cbb60c1c-04ed-4477-bf8e-4dae9fd964ef">CAStoreTypeWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a21b390-4b44-4c50-b11f-1ebf2118f7e8">get_ClientId</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/7a21b390-4b44-4c50-b11f-1ebf2118f7e8">ClientId</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6740378a-342b-4520-89c7-32d44e23cfca">get_ContainerNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/6740378a-342b-4520-89c7-32d44e23cfca">ContainerNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54b85347-cdc1-42e3-bc26-0b50bd58131a">get_DeleteRequestCert</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/54b85347-cdc1-42e3-bc26-0b50bd58131a">DeleteRequestCert</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0571a8c-c682-44fd-a479-ace627b314b5">get_EnableSMIMECapabilities</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/e0571a8c-c682-44fd-a479-ace627b314b5">EnableSMIMECapabilities</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ed181d1-b06f-40f4-892a-80edf327bf40">get_EnableT61DNEncoding</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/7ed181d1-b06f-40f4-892a-80edf327bf40">EnableT61DNEncoding</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6dac3321-9dca-4b7d-8432-e8124bd51db7">get_GenKeyFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/6dac3321-9dca-4b7d-8432-e8124bd51db7">GenKeyFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebf4a7c7-4bd4-4a5f-8f32-bb30a6a8af0e">get_HashAlgID</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/ebf4a7c7-4bd4-4a5f-8f32-bb30a6a8af0e">HashAlgID</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c359c4c8-f53d-48f1-a2ac-9275751b48dc">get_HashAlgorithmWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/c359c4c8-f53d-48f1-a2ac-9275751b48dc">HashAlgorithmWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76b85d63-374c-4ce1-97d4-95f42ddcd53f">get_IncludeSubjectKeyID</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/76b85d63-374c-4ce1-97d4-95f42ddcd53f">IncludeSubjectKeyID</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b05851a0-6228-44e4-9bd7-354c862596e2">get_KeySpec</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/b05851a0-6228-44e4-9bd7-354c862596e2">KeySpec</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53d23dcb-081f-44f4-823f-e3cf79955bc3">get_LimitExchangeKeyToEncipherment</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/53d23dcb-081f-44f4-823f-e3cf79955bc3">LimitExchangeKeyToEncipherment</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e545920a-0c39-49bb-90cc-87039d2e2cfd">get_MyStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/e545920a-0c39-49bb-90cc-87039d2e2cfd">MyStoreFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/077bc593-0071-4f41-8d07-141c9959b6ed">get_MyStoreNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/077bc593-0071-4f41-8d07-141c9959b6ed">MyStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46f95ae3-efd2-4545-b31d-df04112aa737">get_MyStoreTypeWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/46f95ae3-efd2-4545-b31d-df04112aa737">MyStoreTypeWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57e6f86e-fbd3-4fd7-acdd-146a67045ff8">get_ProviderFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/57e6f86e-fbd3-4fd7-acdd-146a67045ff8">ProviderFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42300501-2a64-4433-81e9-6ee3fc31b094">get_ProviderNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/42300501-2a64-4433-81e9-6ee3fc31b094">ProviderNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4ab2b0e-127f-4ec0-9e4a-4314561912e3">get_ProviderType</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/d4ab2b0e-127f-4ec0-9e4a-4314561912e3">ProviderType</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5518c252-fdca-444b-b87e-9fe3cb3b3e3f">get_PVKFileNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/5518c252-fdca-444b-b87e-9fe3cb3b3e3f">PVKFileNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9806cd48-0d95-420b-aa26-0175dd95da46">get_RenewalCertificate</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/9806cd48-0d95-420b-aa26-0175dd95da46">RenewalCertificate</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95ed42ed-04ff-482c-954c-a6c9dd9ccd4c">get_RequestStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/95ed42ed-04ff-482c-954c-a6c9dd9ccd4c">RequestStoreFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ad739c0-fcf7-435b-b427-96ecca1afab7">get_RequestStoreNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/4ad739c0-fcf7-435b-b427-96ecca1afab7">RequestStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b06552a-7b8d-4044-9c2c-994f67e9c36d">get_RequestStoreTypeWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/5b06552a-7b8d-4044-9c2c-994f67e9c36d">RequestStoreTypeWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d67d47f2-9d89-44ba-a5de-e1ae2bc85673">get_ReuseHardwareKeyIfUnableToGenNew</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/d67d47f2-9d89-44ba-a5de-e1ae2bc85673">ReuseHardwareKeyIfUnableToGenNew</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa4640db-f3e5-4fe0-a696-26b5e13b7dd1">get_RootStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/fa4640db-f3e5-4fe0-a696-26b5e13b7dd1">RootStoreFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1b60ba4-974e-43d4-a8f9-8ca619d6b878">get_RootStoreNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/d1b60ba4-974e-43d4-a8f9-8ca619d6b878">RootStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42e50e99-a5ef-40b7-b6ef-c86272d1cd0d">get_RootStoreTypeWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/42e50e99-a5ef-40b7-b6ef-c86272d1cd0d">RootStoreTypeWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75e9327e-72d6-4247-a339-1ca494bc8408">get_SPCFileNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/75e9327e-72d6-4247-a339-1ca494bc8408">SPCFileNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3682e83d-8c3c-42fa-b743-0b149c956339">get_ThumbPrintWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/3682e83d-8c3c-42fa-b743-0b149c956339">ThumbPrintWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1534ec57-71d3-4189-a94e-7bcb3c0670e1">get_UseExistingKeySet</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/1534ec57-71d3-4189-a94e-7bcb3c0670e1">UseExistingKeySet</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07463f0d-f46c-4bc3-8170-0a480b826049">get_WriteCertToCSP</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/07463f0d-f46c-4bc3-8170-0a480b826049">WriteCertToCSP</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b29f442-265f-4826-a2f0-3305d6f70cbb">get_WriteCertToUserDS</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/8b29f442-265f-4826-a2f0-3305d6f70cbb">WriteCertToUserDS</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d628d26-a081-49a2-8fc9-88f014d24a4e">GetAlgNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the name of a cryptographic algorithm given its ID. The values retrieved by this method depend on the current CSP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2545b59e-66ae-48e3-b89f-f214df9d4e6b">getCAStore</a>
</td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04a57bd4-4e04-41eb-97c9-87bfb51be645">getCertContextFromFileResponseWStr</a>
</td>
<td align="left" width="63%">
Retrieves the certificate from a file containing a response from a CA.
			

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3781729d-8b08-41b5-8ff4-1de19fc4ee2e">getCertContextFromPKCS7</a>
</td>
<td align="left" width="63%">
Retrieves the certificate, contained in a PKCS #7 message, that was  issued in response to a PKCS #10 certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/824626bf-a20d-4d34-a061-9f54b142e0fc">getCertContextFromResponseBlob</a>
</td>
<td align="left" width="63%">
Retrieves the certificate from a CA's response.
			
				

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ece7f5a3-e982-48b2-a249-a9c5b5a8a493">GetKeyLen</a>
</td>
<td align="left" width="63%">
Retrieves the minimum and maximum key lengths for the signature and exchange keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/377fed60-7c04-41c1-bc3d-6567d7d8c389">GetKeyLenEx</a>
</td>
<td align="left" width="63%">
Retrieves size information for the signature and exchange keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79e464d2-73f5-4cb2-b3f3-be7d0b1414b4">getMyStore</a>
</td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fdcd4ff-2dd1-4654-9901-a9824d4eddec">GetPrivateKeyArchiveCertificate</a>
</td>
<td align="left" width="63%">
Retrieves the certificate used to archive the private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64d0d96a-b9d4-4b66-8329-2dfc03ba9ce5">getProviderTypeWStr</a>
</td>
<td align="left" width="63%">
Retrieves the type of the specified CSP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc1a61ef-8a5d-4209-9134-f1660cfb6246">getROOTHStore</a>
</td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f7ace8e-0102-4c89-9d8a-e252ad60bb96">GetSupportedKeySpec</a>
</td>
<td align="left" width="63%">
Retrieves information regarding the CSP's support for signature or exchange keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa704c5e-f6ec-4187-b787-7b15cc7d4eb4">InstallPKCS7Blob</a>
</td>
<td align="left" width="63%">
Processes a certificate or chain of certificates, placing them into the appropriate <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate stores</a>. This method differs from the  <a href="https://msdn.microsoft.com/8772f528-2c33-48f4-bb0c-cfde91cf2fba">acceptPKCS7Blob</a> method in that  <a href="https://msdn.microsoft.com/fa704c5e-f6ec-4187-b787-7b15cc7d4eb4">InstallPKCS7Blob</a> does not receive a request certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a65eac6-3fe5-4464-876d-80eedaca7ae6">InstallPKCS7BlobEx</a>
</td>
<td align="left" width="63%">
Extends  
<a href="https://msdn.microsoft.com/fa704c5e-f6ec-4187-b787-7b15cc7d4eb4">InstallPKCS7Blob</a>  by returning the number of certificates actually installed in local stores.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/294a8a38-9c76-4e5c-ac11-2fcb8b81727e">put_CAStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/294a8a38-9c76-4e5c-ac11-2fcb8b81727e">CAStoreFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c016649-a780-45c1-94a4-fb08c15c4e0f">put_CAStoreNameWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/4c016649-a780-45c1-94a4-fb08c15c4e0f">CAStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbb60c1c-04ed-4477-bf8e-4dae9fd964ef">put_CAStoreTypeWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/cbb60c1c-04ed-4477-bf8e-4dae9fd964ef">CAStoreTypeWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a21b390-4b44-4c50-b11f-1ebf2118f7e8">put_ClientId</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/7a21b390-4b44-4c50-b11f-1ebf2118f7e8">ClientId</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6740378a-342b-4520-89c7-32d44e23cfca">put_ContainerNameWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/6740378a-342b-4520-89c7-32d44e23cfca">ContainerNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54b85347-cdc1-42e3-bc26-0b50bd58131a">put_DeleteRequestCert</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/54b85347-cdc1-42e3-bc26-0b50bd58131a">DeleteRequestCert</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0571a8c-c682-44fd-a479-ace627b314b5">put_EnableSMIMECapabilities</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/e0571a8c-c682-44fd-a479-ace627b314b5">EnableSMIMECapabilities</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ed181d1-b06f-40f4-892a-80edf327bf40">put_EnableT61DNEncoding</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/7ed181d1-b06f-40f4-892a-80edf327bf40">EnableT61DNEncoding</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6dac3321-9dca-4b7d-8432-e8124bd51db7">put_GenKeyFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/6dac3321-9dca-4b7d-8432-e8124bd51db7">GenKeyFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebf4a7c7-4bd4-4a5f-8f32-bb30a6a8af0e">put_HashAlgID</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/ebf4a7c7-4bd4-4a5f-8f32-bb30a6a8af0e">HashAlgID</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c359c4c8-f53d-48f1-a2ac-9275751b48dc">put_HashAlgorithmWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/c359c4c8-f53d-48f1-a2ac-9275751b48dc">HashAlgorithmWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76b85d63-374c-4ce1-97d4-95f42ddcd53f">put_IncludeSubjectKeyID</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/76b85d63-374c-4ce1-97d4-95f42ddcd53f">IncludeSubjectKeyID</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b05851a0-6228-44e4-9bd7-354c862596e2">put_KeySpec</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/b05851a0-6228-44e4-9bd7-354c862596e2">KeySpec</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53d23dcb-081f-44f4-823f-e3cf79955bc3">put_LimitExchangeKeyToEncipherment</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/53d23dcb-081f-44f4-823f-e3cf79955bc3">LimitExchangeKeyToEncipherment</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e545920a-0c39-49bb-90cc-87039d2e2cfd">put_MyStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/e545920a-0c39-49bb-90cc-87039d2e2cfd">MyStoreFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/077bc593-0071-4f41-8d07-141c9959b6ed">put_MyStoreNameWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/077bc593-0071-4f41-8d07-141c9959b6ed">MyStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46f95ae3-efd2-4545-b31d-df04112aa737">put_MyStoreTypeWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/46f95ae3-efd2-4545-b31d-df04112aa737">MyStoreTypeWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57e6f86e-fbd3-4fd7-acdd-146a67045ff8">put_ProviderFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/57e6f86e-fbd3-4fd7-acdd-146a67045ff8">ProviderFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42300501-2a64-4433-81e9-6ee3fc31b094">put_ProviderNameWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/42300501-2a64-4433-81e9-6ee3fc31b094">ProviderNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4ab2b0e-127f-4ec0-9e4a-4314561912e3">put_ProviderType</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/d4ab2b0e-127f-4ec0-9e4a-4314561912e3">ProviderType</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5518c252-fdca-444b-b87e-9fe3cb3b3e3f">put_PVKFileNameWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/5518c252-fdca-444b-b87e-9fe3cb3b3e3f">PVKFileNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9806cd48-0d95-420b-aa26-0175dd95da46">put_RenewalCertificate</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/9806cd48-0d95-420b-aa26-0175dd95da46">RenewalCertificate</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95ed42ed-04ff-482c-954c-a6c9dd9ccd4c">put_RequestStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/95ed42ed-04ff-482c-954c-a6c9dd9ccd4c">RequestStoreFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ad739c0-fcf7-435b-b427-96ecca1afab7">put_RequestStoreNameWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/4ad739c0-fcf7-435b-b427-96ecca1afab7">RequestStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b06552a-7b8d-4044-9c2c-994f67e9c36d">put_RequestStoreTypeWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/5b06552a-7b8d-4044-9c2c-994f67e9c36d">RequestStoreTypeWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d67d47f2-9d89-44ba-a5de-e1ae2bc85673">put_ReuseHardwareKeyIfUnableToGenNew</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/d67d47f2-9d89-44ba-a5de-e1ae2bc85673">ReuseHardwareKeyIfUnableToGenNew</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa4640db-f3e5-4fe0-a696-26b5e13b7dd1">put_RootStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/fa4640db-f3e5-4fe0-a696-26b5e13b7dd1">RootStoreFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1b60ba4-974e-43d4-a8f9-8ca619d6b878">put_RootStoreNameWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/d1b60ba4-974e-43d4-a8f9-8ca619d6b878">RootStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42e50e99-a5ef-40b7-b6ef-c86272d1cd0d">put_RootStoreTypeWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/42e50e99-a5ef-40b7-b6ef-c86272d1cd0d">RootStoreTypeWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75e9327e-72d6-4247-a339-1ca494bc8408">put_SPCFileNameWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/75e9327e-72d6-4247-a339-1ca494bc8408">SPCFileNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3682e83d-8c3c-42fa-b743-0b149c956339">put_ThumbPrintWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/3682e83d-8c3c-42fa-b743-0b149c956339">ThumbPrintWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1534ec57-71d3-4189-a94e-7bcb3c0670e1">put_UseExistingKeySet</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/1534ec57-71d3-4189-a94e-7bcb3c0670e1">UseExistingKeySet</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07463f0d-f46c-4bc3-8170-0a480b826049">put_WriteCertToCSP</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/07463f0d-f46c-4bc3-8170-0a480b826049">WriteCertToCSP</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b29f442-265f-4826-a2f0-3305d6f70cbb">put_WriteCertToUserDS</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/8b29f442-265f-4826-a2f0-3305d6f70cbb">WriteCertToUserDS</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e00fad2-dc06-421d-9a8c-27c5a951466c">removePendingRequestWStr</a>
</td>
<td align="left" width="63%">
Removes a pending request from the client's request store.
				

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
 Returns the certificate enrollment control  object to its initial <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9da2371-441e-45c7-9723-39d01b6ece27">resetAttributes</a>
</td>
<td align="left" width="63%">
Removes all attributes from the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e03ecaa-3996-4aea-b328-e438194f30d5">resetExtensions</a>
</td>
<td align="left" width="63%">
Removes all extensions from the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d70fa8c0-7cdf-4023-9700-68f24d9116af">SetHStoreCA</a>
</td>
<td align="left" width="63%">
Specifies the handle to use for the CA store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/669c8fe4-def3-41c5-82fc-95c26f3950c8">SetHStoreMy</a>
</td>
<td align="left" width="63%">
Specifies the handle to use for the MY store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7424d94f-8f81-432a-b003-a1c30fcc70ae">SetHStoreRequest</a>
</td>
<td align="left" width="63%">
Specifies the handle to use for the request store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d41fabce-e0f8-4e82-b177-59a10af376ab">SetHStoreROOT</a>
</td>
<td align="left" width="63%">
Specifies the handle to use for the ROOT store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02b49033-3354-4e30-a816-a9c078c6164a">setPendingRequestInfoWStr</a>
</td>
<td align="left" width="63%">
Sets properties for a pending request.
				

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e37a8055-4074-425b-8f88-69b898855824">SetPrivateKeyArchiveCertificate</a>
</td>
<td align="left" width="63%">
Specifies the certificate used to archive the private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c970f6b-6b8f-4396-b59b-d6b58d52172b">SetSignerCertificate</a>
</td>
<td align="left" width="63%">
Specifies the signer's certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b15df753-77c5-4746-a6a5-ddbf3cc8158f">stringToBinaryBlob</a>
</td>
<td align="left" width="63%">
Converts a string to a  binary data BLOB.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnroll4</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/294a8a38-9c76-4e5c-ac11-2fcb8b81727e">CAStoreFlags</a>


</td>
<td align="left" width="63%">
Sets or retrieves a flag that controls the certificate store when it is opened.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4c016649-a780-45c1-94a4-fb08c15c4e0f">CAStoreNameWStr</a>


</td>
<td align="left" width="63%">
 Sets or retrieves the name of the store where all non-"ROOT" and non-"MY" certificates are kept.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cbb60c1c-04ed-4477-bf8e-4dae9fd964ef">CAStoreTypeWStr</a>


</td>
<td align="left" width="63%">
Sets or retrieves the type of store to use for the store specified by the 
<a href="https://msdn.microsoft.com/4c016649-a780-45c1-94a4-fb08c15c4e0f">CAStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7a21b390-4b44-4c50-b11f-1ebf2118f7e8">ClientId</a>


</td>
<td align="left" width="63%">
Sets or retrieves the client ID request attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6740378a-342b-4520-89c7-32d44e23cfca">ContainerNameWStr</a>


</td>
<td align="left" width="63%">
Sets or retrieves the  name of the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key container</a> to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/54b85347-cdc1-42e3-bc26-0b50bd58131a">DeleteRequestCert</a>


</td>
<td align="left" width="63%">
Sets or retrieves a Boolean indicator that controls whether dummy certificates in the request store are deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e0571a8c-c682-44fd-a479-ace627b314b5">EnableSMIMECapabilities</a>


</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that controls whether the PKCS #10 will contain a signed attribute for <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Secure/Multipurpose Internet Mail Extensions</a> (S/MIME) capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7ed181d1-b06f-40f4-892a-80edf327bf40">EnableT61DNEncoding</a>


</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that controls whether the distinguished name in the request is encoded as a T61 string instead of as a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6dac3321-9dca-4b7d-8432-e8124bd51db7">GenKeyFlags</a>


</td>
<td align="left" width="63%">
Sets or retrieves the values passed to <a href="https://msdn.microsoft.com/b65dd856-2dfa-4cda-9b2f-b32f3c291470">CryptGenKey</a> when the certificate request is generated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ebf4a7c7-4bd4-4a5f-8f32-bb30a6a8af0e">HashAlgID</a>


</td>
<td align="left" width="63%">
Sets or retrieves the hash algorithm used when signing a PKCS #10 certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c359c4c8-f53d-48f1-a2ac-9275751b48dc">HashAlgorithmWStr</a>


</td>
<td align="left" width="63%">
Sets or retrieves only the signature hash algorithm used to sign the PKCS #10.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/76b85d63-374c-4ce1-97d4-95f42ddcd53f">IncludeSubjectKeyID</a>


</td>
<td align="left" width="63%">
Specifies whether the subject key ID extension is added to the certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b05851a0-6228-44e4-9bd7-354c862596e2">KeySpec</a>


</td>
<td align="left" width="63%">
Sets or retrieves the  type of key generated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/53d23dcb-081f-44f4-823f-e3cf79955bc3">LimitExchangeKeyToEncipherment</a>


</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that controls whether an AT_KEYEXCHANGE request contains <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">digital signature</a> and non-repudiation key usages. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e545920a-0c39-49bb-90cc-87039d2e2cfd">MyStoreFlags</a>


</td>
<td align="left" width="63%">
Sets or retrieves the registry location used for the MY store. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/077bc593-0071-4f41-8d07-141c9959b6ed">MyStoreNameWStr</a>


</td>
<td align="left" width="63%">
 Sets or retrieves the name of the store  where certificates with linked private keys are kept.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/46f95ae3-efd2-4545-b31d-df04112aa737">MyStoreTypeWStr</a>


</td>
<td align="left" width="63%">
Sets or retrieves the type of store  specified by the 
<a href="https://msdn.microsoft.com/077bc593-0071-4f41-8d07-141c9959b6ed">MyStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/57e6f86e-fbd3-4fd7-acdd-146a67045ff8">ProviderFlags</a>


</td>
<td align="left" width="63%">
 Sets or retrieves the CSP type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/42300501-2a64-4433-81e9-6ee3fc31b094">ProviderNameWStr</a>


</td>
<td align="left" width="63%">
 Sets or retrieves the name of the CSP to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d4ab2b0e-127f-4ec0-9e4a-4314561912e3">ProviderType</a>


</td>
<td align="left" width="63%">
 Sets or retrieves the type of provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5518c252-fdca-444b-b87e-9fe3cb3b3e3f">PVKFileNameWStr</a>


</td>
<td align="left" width="63%">
 Sets or retrieves the name of the file that will contain exported keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9806cd48-0d95-420b-aa26-0175dd95da46">RenewalCertificate</a>


</td>
<td align="left" width="63%">
Specifies the certificate context for the renewal certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/95ed42ed-04ff-482c-954c-a6c9dd9ccd4c">RequestStoreFlags</a>


</td>
<td align="left" width="63%">
Sets or retrieves the registry location used for the REQUEST store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4ad739c0-fcf7-435b-b427-96ecca1afab7">RequestStoreNameWStr</a>


</td>
<td align="left" width="63%">
Sets or retrieves the name of the store that contains the dummy certificate. This dummy certificate, along with the added private keys, remains in the request store  until a certification authority processes the request and responds with a PKCS #7.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5b06552a-7b8d-4044-9c2c-994f67e9c36d">RequestStoreTypeWStr</a>


</td>
<td align="left" width="63%">
 Sets or retrieves the type of store to use for the store specified by the 
<a href="https://msdn.microsoft.com/4ad739c0-fcf7-435b-b427-96ecca1afab7">RequestStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d67d47f2-9d89-44ba-a5de-e1ae2bc85673">ReuseHardwareKeyIfUnableToGenNew</a>


</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that determines the action taken by the 
certificate enrollment control object if an error is encountered when generating a new key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fa4640db-f3e5-4fe0-a696-26b5e13b7dd1">RootStoreFlags</a>


</td>
<td align="left" width="63%">
Sets or retrieves the registry location used for the ROOT store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d1b60ba4-974e-43d4-a8f9-8ca619d6b878">RootStoreNameWStr</a>


</td>
<td align="left" width="63%">
Sets or retrieves the name of the root store where all intrinsically trusted self-signed ROOT certificates are kept.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/42e50e99-a5ef-40b7-b6ef-c86272d1cd0d">RootStoreTypeWStr</a>


</td>
<td align="left" width="63%">
Sets or retrieves the type of store to use for the store specified by the 
<a href="https://msdn.microsoft.com/d1b60ba4-974e-43d4-a8f9-8ca619d6b878">RootStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/75e9327e-72d6-4247-a339-1ca494bc8408">SPCFileNameWStr</a>


</td>
<td align="left" width="63%">
Sets or retrieves the name of the file to write the resulting base64-encoded PKCS #7 as returned from the certification authority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3682e83d-8c3c-42fa-b743-0b149c956339">ThumbPrintWStr</a>


</td>
<td align="left" width="63%">
Sets or retrieves a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of the certificate data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1534ec57-71d3-4189-a94e-7bcb3c0670e1">UseExistingKeySet</a>


</td>
<td align="left" width="63%">
 Sets or retrieves a Boolean value that indicates whether the existing keys should be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/07463f0d-f46c-4bc3-8170-0a480b826049">WriteCertToCSP</a>


</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that indicates whether a certificate should be written to the CSP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8b29f442-265f-4826-a2f0-3305d6f70cbb">WriteCertToUserDS</a>


</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that controls whether the certificate is written to the user's Active Directory store.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a>



<a href="https://msdn.microsoft.com/60a28944-35de-4ea2-8523-5634685ac224">IEnroll2</a>
 

 

