---
UID: NN:xenroll.ICEnroll4
title: ICEnroll4
author: windows-sdk-content
description: The ICEnroll4 interface is one of several interfaces that represent the Certificate Enrollment Control.
old-location: security\icenroll4.htm
tech.root: seccrypto
ms.assetid: 4e3e3792-aa41-46fe-bf75-26c2b8959f7a
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ICEnroll4, ICEnroll4 interface [Security], ICEnroll4 interface [Security],described, _xen_icenroll4, security.icenroll4, xenroll/ICEnroll4
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll4 interface


## -description


<p class="CCE_Message">[This interface is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ICEnroll4</b> interface is one of several interfaces that represent the Certificate Enrollment Control. It is primarily of interest if you are not using Automation. If, on the other hand, you are programming in Visual Basic or another Automation language, see the 
<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICEnroll4</b> interface inherits from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>, <a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a>, <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>, and <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>. <b>ICEnroll4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICEnroll4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dae9f6b8-6690-47cc-9397-168c1ff54c55">acceptFilePKCS7</a>
</td>
<td align="left" width="63%">
Accepts and processes a file that contains a PKCS #7 message containing a certificate.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/127863ca-843b-46c5-b375-fb0400e8b49b">acceptFileResponse</a>
</td>
<td align="left" width="63%">
Accepts delivery of the credentials issued in response to an earlier call to 
<a href="https://msdn.microsoft.com/8902eb8e-c597-42a6-8836-6a24181da4d4">createFileRequest</a>, and it places the credentials in the appropriate store.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a428d83-c846-4f44-a682-58c3e025c353">acceptPKCS7</a>
</td>
<td align="left" width="63%">
Accepts and processes a PKCS #7 message containing a certificate. The PKCS #7 is input as a parameter.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1149a76e-e714-4bc7-842c-6fcbe220cd24">acceptResponse</a>
</td>
<td align="left" width="63%">
Accepts delivery of the credentials issued in response to an earlier call to 
<a href="https://msdn.microsoft.com/d2a1c1c4-dbbf-423c-bf59-da0ab9a71078">createRequest</a> and places the credentials in the appropriate store.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a15fe06c-e2a5-4292-ad82-ea350e652a07">addAttributeToRequest</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a> to the certificate request.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a21e2636-d49f-4490-867c-2ea95d7fdc69">addBlobPropertyToCertificate</a>
</td>
<td align="left" width="63%">
Adds a <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> property to a certificate.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2c22689-d386-43d1-a42f-f303a034a087">addCertTypeToRequest</a>
</td>
<td align="left" width="63%">
Adds a certificate template to a request (used to support the enterprise <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA)).</p> (Inherited from <a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bde35e01-8b26-44f7-828e-e8313a2b5a12">addCertTypeToRequestEx</a>
</td>
<td align="left" width="63%">
Adds a certificate template (or "certificate type") to a request.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bd46cd6-cc7e-4d87-b8ff-8fa01f639282">addExtensionToRequest</a>
</td>
<td align="left" width="63%">
Adds an extension to the request.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/252d1789-1207-4281-b044-e1f1ca6cd585">addNameValuePairToRequest</a>
</td>
<td align="left" width="63%">
Adds a name-value string pair to the request.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a31975f7-432e-47bb-a24e-508c6ca85373">addNameValuePairToSignature</a>
</td>
<td align="left" width="63%">
Adds the name and value pair of an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a> to the request. It is up to the CA to interpret the meaning of the name-value pair.</p> (Inherited from <a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43358d84-ccdd-49a8-be1d-bb5e8ddd1397">binaryToString</a>
</td>
<td align="left" width="63%">
Converts a binary data <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> to a string.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df58ba41-5301-48dd-9255-7173bb73965c">createFilePFX</a>
</td>
<td align="left" width="63%">
Saves the accepted certificate chain and <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> in a file in Personal Information Exchange (PFX) format.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/074c7321-6117-4261-836a-a2055c9e029d">createFilePKCS10</a>
</td>
<td align="left" width="63%">
Creates a base64-encoded PKCS #10 <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a> and saves it in a file.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8902eb8e-c597-42a6-8836-6a24181da4d4">createFileRequest</a>
</td>
<td align="left" width="63%">
Creates a PKCS #10 certificate request, a PKCS #7 request, or a full CMC request and stores it in a file.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37b69fc6-db16-4491-b596-4ef76e5414b3">createPFX</a>
</td>
<td align="left" width="63%">
Saves the accepted certificate chain and private key in a PFX format string. The PFX format is also known as PKCS #12.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8e841c1-f16e-4f3a-94f2-ef6708c88910">createPKCS10</a>
</td>
<td align="left" width="63%">
Creates a base64-encoded PKCS #10 certificate request.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2a1c1c4-dbbf-423c-bf59-da0ab9a71078">createRequest</a>
</td>
<td align="left" width="63%">
Creates a PKCS #10, PKCS #7, or full <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Management over CMS</a> (CMC) format certificate request and stores it in a string.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7fe4abc-38e8-42a0-a7a0-312ccfc309e5">EnumAlgs</a>
</td>
<td align="left" width="63%">
Retrieves the IDs of cryptographic algorithms in a given algorithm class that are supported by the current CSP.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28102a55-3bda-4413-84b6-cfa2057be98b">enumContainers</a>
</td>
<td align="left" width="63%">
Retrieves the names of the containers for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) specified by the 
<a href="https://msdn.microsoft.com/092d5ed1-8d03-45d8-bc7a-3e27035f4b2f">ProviderName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/566974d1-79ec-4cbd-ae84-85e0a78edf58">enumPendingRequest</a>
</td>
<td align="left" width="63%">
Enumerates pending certificate requests and retrieves a specified property from each.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05188aee-2b03-46bc-89f4-506a019496a4">enumProviders</a>
</td>
<td align="left" width="63%">
Retrieves the names of the available CSPs specified by the 
<a href="https://msdn.microsoft.com/90daa97a-350e-4307-80a5-b018cc1f0e86">ProviderType</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d3fd4d4-779f-4e28-9b07-4de17262ac5e">freeRequestInfo</a>
</td>
<td align="left" width="63%">
Cleans up the stores if an error occurs. Currently not implemented.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cde75e0f-5074-44f7-a101-f503913a58f4">get_CAStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/cde75e0f-5074-44f7-a101-f503913a58f4">CAStoreFlags</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29616175-7195-430e-a85b-99b50e276e7f">get_CAStoreName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/29616175-7195-430e-a85b-99b50e276e7f">CAStoreName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b0b113d-4046-4b2b-8f3b-ad08bfe3d0ac">get_CAStoreType</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/8b0b113d-4046-4b2b-8f3b-ad08bfe3d0ac">CAStoreType</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf46af62-815a-4ad5-bca9-e81eb7c0d1e2">get_ClientId</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/cf46af62-815a-4ad5-bca9-e81eb7c0d1e2">ClientId</a> property.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa863843-8bbc-47c5-9d58-b64fb6703c0a">get_ContainerName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/fa863843-8bbc-47c5-9d58-b64fb6703c0a">ContainerName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f026f4ed-e003-4ece-8c08-427dac48229f">get_DeleteRequestCert</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/f026f4ed-e003-4ece-8c08-427dac48229f">DeleteRequestCert</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/057033ab-f2e0-4d60-b47f-73973f82f806">get_EnableSMIMECapabilities</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/057033ab-f2e0-4d60-b47f-73973f82f806">EnableSMIMECapabilities</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff8fe103-0303-4f40-af25-efa50155c36f">get_EnableT61DNEncoding</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/ff8fe103-0303-4f40-af25-efa50155c36f">EnableT61DNEncoding</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d22fe4d4-a939-4f77-8e11-f9312c81ec1e">get_GenKeyFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/d22fe4d4-a939-4f77-8e11-f9312c81ec1e">GenKeyFlags</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46f371a3-7254-4f54-b147-402f2a37e277">get_HashAlgID</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/46f371a3-7254-4f54-b147-402f2a37e277">HashAlgID</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48f8a47b-0ab4-4150-b8cf-37e57fb04d3e">get_HashAlgorithm</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/48f8a47b-0ab4-4150-b8cf-37e57fb04d3e">HashAlgorithm</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12150ca2-59cc-402e-b25e-cc98b940ecf8">get_IncludeSubjectKeyID</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/12150ca2-59cc-402e-b25e-cc98b940ecf8">IncludeSubjectKeyID</a> property.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30cc7c86-29ce-42e9-b9dc-d29f5b5450a5">get_KeySpec</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/30cc7c86-29ce-42e9-b9dc-d29f5b5450a5">KeySpec</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8ed3663-bbda-4052-9c72-b00543ca73ab">get_LimitExchangeKeyToEncipherment</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/d8ed3663-bbda-4052-9c72-b00543ca73ab">LimitExchangeKeyToEncipherment</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0616c666-9cfc-48f9-93a2-91d51d8dff04">get_MyStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/0616c666-9cfc-48f9-93a2-91d51d8dff04">MyStoreFlags</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa08e88d-bd1f-4bd6-806e-56f720846623">get_MyStoreName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/aa08e88d-bd1f-4bd6-806e-56f720846623">MyStoreName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/948a9012-b2ac-4bf0-8cae-690ea3ecdb2e">get_MyStoreType</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/948a9012-b2ac-4bf0-8cae-690ea3ecdb2e">MyStoreType</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5099bef-2882-4106-a2e6-a144e16993c3">get_PrivateKeyArchiveCertificate</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/c5099bef-2882-4106-a2e6-a144e16993c3">PrivateKeyArchiveCertificate</a> property.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddf92921-368f-4769-b2c1-b9d6a94b0fcb">get_ProviderFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/ddf92921-368f-4769-b2c1-b9d6a94b0fcb">ProviderFlags</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/092d5ed1-8d03-45d8-bc7a-3e27035f4b2f">get_ProviderName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/092d5ed1-8d03-45d8-bc7a-3e27035f4b2f">ProviderName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90daa97a-350e-4307-80a5-b018cc1f0e86">get_ProviderType</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/90daa97a-350e-4307-80a5-b018cc1f0e86">ProviderType</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f841bb2-6cfd-4712-bb71-5c3d9d462fab">get_PVKFileName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/3f841bb2-6cfd-4712-bb71-5c3d9d462fab">PVKFileName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/399870f0-69e1-4a21-a7fa-c3de9ee66876">get_RequestStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/399870f0-69e1-4a21-a7fa-c3de9ee66876">RequestStoreFlags</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03">get_RequestStoreName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03">RequestStoreName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc0d09bc-3589-454d-a1fe-141af46bc45b">get_RequestStoreType</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/cc0d09bc-3589-454d-a1fe-141af46bc45b">RequestStoreType</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a9d5f78-bf88-4e24-9685-7c504f9f2e38">get_ReuseHardwareKeyIfUnableToGenNew</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/5a9d5f78-bf88-4e24-9685-7c504f9f2e38">ReuseHardwareKeyIfUnableToGenNew</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf844047-4f5a-42de-a446-195371c0dbcf">get_RootStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/bf844047-4f5a-42de-a446-195371c0dbcf">RootStoreFlags</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b686ade-e8ee-4c59-ab90-05088f575acd">get_RootStoreName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/5b686ade-e8ee-4c59-ab90-05088f575acd">RootStoreName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/452f89ad-e512-4ac7-816a-c3f97e25350a">get_RootStoreType</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/452f89ad-e512-4ac7-816a-c3f97e25350a">RootStoreType</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ff2f111-31bd-4ed4-a335-2db536477660">get_SPCFileName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/4ff2f111-31bd-4ed4-a335-2db536477660">SPCFileName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58f027c6-fa92-40ac-b41d-89b6fba7455d">get_ThumbPrint</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/58f027c6-fa92-40ac-b41d-89b6fba7455d">ThumbPrint</a> property.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5115033-bda1-4160-84b3-80c692bf64fb">get_UseExistingKeySet</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/e5115033-bda1-4160-84b3-80c692bf64fb">UseExistingKeySet</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc622f5b-e6d0-48c5-8535-29d6d4b02129">get_WriteCertToCSP</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/cc622f5b-e6d0-48c5-8535-29d6d4b02129">WriteCertToCSP</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c80f6b9-f5f7-4fa1-9cb5-db19cdc9ec25">get_WriteCertToUserDS</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/8c80f6b9-f5f7-4fa1-9cb5-db19cdc9ec25">WriteCertToUserDS</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c5fa25c-7fab-4fb5-9ff6-bc7379260926">GetAlgName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a cryptographic algorithm given its ID. The values retrieved by this method depend on the current CSP.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e89465b-4525-4b36-b0c7-7f34dc4a34aa">getCertFromFileResponse</a>
</td>
<td align="left" width="63%">
Retrieves the certificate from a file containing a response from a CA.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3094cd58-d123-40f1-ac81-dffdfb56d47d">getCertFromPKCS7</a>
</td>
<td align="left" width="63%">
Retrieves the certificate, contained in a PKCS #7 message, that was  issued in response to a PKCS #10 certificate request.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e2b1f53-c6fc-4fb8-a69c-58ab8ac6f258">getCertFromResponse</a>
</td>
<td align="left" width="63%">
Retrieves the certificate from a CA's response.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d4cde68-f47c-46ad-a0ca-ee287f6e5bed">GetKeyLen</a>
</td>
<td align="left" width="63%">
Retrieves the minimum and maximum key lengths for the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">signature</a> and <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">exchange keys</a>.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e54926f-f600-4795-b6d8-efb146edcda2">GetKeyLenEx</a>
</td>
<td align="left" width="63%">
Retrieves size information for the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">signature</a> and <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">exchange keys</a>.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f47c07b8-0919-44d4-b331-e062341aa050">getProviderType</a>
</td>
<td align="left" width="63%">
Retrieves the type of the specified CSP.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e225eddb-0c36-446a-9696-38653ff22511">GetSupportedKeySpec</a>
</td>
<td align="left" width="63%">
Retrieves information regarding the CSP's support for signature or exchange keys.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63482360-0d8a-4e23-8942-8276630778a3">InstallPKCS7</a>
</td>
<td align="left" width="63%">
Processes a certificate or chain of certificates, placing them into the appropriate <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate stores</a>. This method differs from the  <a href="https://msdn.microsoft.com/5a428d83-c846-4f44-a682-58c3e025c353">acceptPKCS7</a> method in that  <a href="https://msdn.microsoft.com/63482360-0d8a-4e23-8942-8276630778a3">InstallPKCS7</a> does not receive a request certificate.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/886fd5f0-d91f-439f-b259-dfb0206d3078">InstallPKCS7Ex</a>
</td>
<td align="left" width="63%">
The same as 
<a href="https://msdn.microsoft.com/63482360-0d8a-4e23-8942-8276630778a3">InstallPKCS7</a> except that it returns the number of certificates actually installed in local stores.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0616c666-9cfc-48f9-93a2-91d51d8dff04">put MyStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/0616c666-9cfc-48f9-93a2-91d51d8dff04">MyStoreFlags</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cde75e0f-5074-44f7-a101-f503913a58f4">put_CAStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/cde75e0f-5074-44f7-a101-f503913a58f4">CAStoreFlags</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29616175-7195-430e-a85b-99b50e276e7f">put_CAStoreName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/29616175-7195-430e-a85b-99b50e276e7f">CAStoreName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b0b113d-4046-4b2b-8f3b-ad08bfe3d0ac">put_CAStoreType</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/8b0b113d-4046-4b2b-8f3b-ad08bfe3d0ac">CAStoreType</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf46af62-815a-4ad5-bca9-e81eb7c0d1e2">put_ClientId</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/cf46af62-815a-4ad5-bca9-e81eb7c0d1e2">ClientId</a> property.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa863843-8bbc-47c5-9d58-b64fb6703c0a">put_ContainerName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/fa863843-8bbc-47c5-9d58-b64fb6703c0a">ContainerName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f026f4ed-e003-4ece-8c08-427dac48229f">put_DeleteRequestCert</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/f026f4ed-e003-4ece-8c08-427dac48229f">DeleteRequestCert</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/057033ab-f2e0-4d60-b47f-73973f82f806">put_EnableSMIMECapabilities</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/057033ab-f2e0-4d60-b47f-73973f82f806">EnableSMIMECapabilities</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff8fe103-0303-4f40-af25-efa50155c36f">put_EnableT61DNEncoding</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/ff8fe103-0303-4f40-af25-efa50155c36f">EnableT61DNEncoding</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d22fe4d4-a939-4f77-8e11-f9312c81ec1e">put_GenKeyFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/d22fe4d4-a939-4f77-8e11-f9312c81ec1e">GenKeyFlags</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46f371a3-7254-4f54-b147-402f2a37e277">put_HashAlgID</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/46f371a3-7254-4f54-b147-402f2a37e277">HashAlgID</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48f8a47b-0ab4-4150-b8cf-37e57fb04d3e">put_HashAlgorithm</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/48f8a47b-0ab4-4150-b8cf-37e57fb04d3e">HashAlgorithm</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12150ca2-59cc-402e-b25e-cc98b940ecf8">put_IncludeSubjectKeyID</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/12150ca2-59cc-402e-b25e-cc98b940ecf8">IncludeSubjectKeyID</a> property.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30cc7c86-29ce-42e9-b9dc-d29f5b5450a5">put_KeySpec</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/30cc7c86-29ce-42e9-b9dc-d29f5b5450a5">KeySpec</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8ed3663-bbda-4052-9c72-b00543ca73ab">put_LimitExchangeKeyToEncipherment</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/d8ed3663-bbda-4052-9c72-b00543ca73ab">LimitExchangeKeyToEncipherment</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa08e88d-bd1f-4bd6-806e-56f720846623">put_MyStoreName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/aa08e88d-bd1f-4bd6-806e-56f720846623">MyStoreName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/948a9012-b2ac-4bf0-8cae-690ea3ecdb2e">put_MyStoreType</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/948a9012-b2ac-4bf0-8cae-690ea3ecdb2e">MyStoreType</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5099bef-2882-4106-a2e6-a144e16993c3">put_PrivateKeyArchiveCertificate</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/c5099bef-2882-4106-a2e6-a144e16993c3">PrivateKeyArchiveCertificate</a> property.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddf92921-368f-4769-b2c1-b9d6a94b0fcb">put_ProviderFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/ddf92921-368f-4769-b2c1-b9d6a94b0fcb">ProviderFlags</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/092d5ed1-8d03-45d8-bc7a-3e27035f4b2f">put_ProviderName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/092d5ed1-8d03-45d8-bc7a-3e27035f4b2f">ProviderName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90daa97a-350e-4307-80a5-b018cc1f0e86">put_ProviderType</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/90daa97a-350e-4307-80a5-b018cc1f0e86">ProviderType</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f841bb2-6cfd-4712-bb71-5c3d9d462fab">put_PVKFileName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/3f841bb2-6cfd-4712-bb71-5c3d9d462fab">PVKFileName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/399870f0-69e1-4a21-a7fa-c3de9ee66876">put_RequestStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/399870f0-69e1-4a21-a7fa-c3de9ee66876">RequestStoreFlags</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03">put_RequestStoreName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03">RequestStoreName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc0d09bc-3589-454d-a1fe-141af46bc45b">put_RequestStoreType</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/cc0d09bc-3589-454d-a1fe-141af46bc45b">RequestStoreType</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a9d5f78-bf88-4e24-9685-7c504f9f2e38">put_ReuseHardwareKeyIfUnableToGenNew</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/5a9d5f78-bf88-4e24-9685-7c504f9f2e38">ReuseHardwareKeyIfUnableToGenNew</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf844047-4f5a-42de-a446-195371c0dbcf">put_RootStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/bf844047-4f5a-42de-a446-195371c0dbcf">RootStoreFlags</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b686ade-e8ee-4c59-ab90-05088f575acd">put_RootStoreName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/5b686ade-e8ee-4c59-ab90-05088f575acd">RootStoreName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/452f89ad-e512-4ac7-816a-c3f97e25350a">put_RootStoreType</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/452f89ad-e512-4ac7-816a-c3f97e25350a">RootStoreType</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e5b8964-f737-407e-b265-fe095bd6f8ad">put_SignerCertificate</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/3e5b8964-f737-407e-b265-fe095bd6f8ad">SignerCertificate</a> property.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ff2f111-31bd-4ed4-a335-2db536477660">put_SPCFileName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/4ff2f111-31bd-4ed4-a335-2db536477660">SPCFileName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58f027c6-fa92-40ac-b41d-89b6fba7455d">put_ThumbPrint</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/58f027c6-fa92-40ac-b41d-89b6fba7455d">ThumbPrint</a> property.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5115033-bda1-4160-84b3-80c692bf64fb">put_UseExistingKeySet</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/e5115033-bda1-4160-84b3-80c692bf64fb">UseExistingKeySet</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc622f5b-e6d0-48c5-8535-29d6d4b02129">put_WriteCertToCSP</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/cc622f5b-e6d0-48c5-8535-29d6d4b02129">WriteCertToCSP</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c80f6b9-f5f7-4fa1-9cb5-db19cdc9ec25">put_WriteCertToUserDS</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/8c80f6b9-f5f7-4fa1-9cb5-db19cdc9ec25">WriteCertToUserDS</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22ddd7f8-b2c0-4b9a-a2b3-c2cb470d0502">removePendingRequest</a>
</td>
<td align="left" width="63%">
Removes a pending request from the client's request store.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/503062c3-8a73-4218-a826-c72f926f36db">Reset</a>
</td>
<td align="left" width="63%">
 Returns the certificate enrollment control  object to its initial <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a>.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/606cc93a-cc18-43fb-94e7-dc35dc7f2533">resetAttributes</a>
</td>
<td align="left" width="63%">
 Removes all attributes from the request.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ee3c056-27b0-4606-bdf6-63e5e4439274">resetBlobProperties</a>
</td>
<td align="left" width="63%">
Resets the properties of a <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef21a5e4-2641-4602-b1ae-f0f74b9a8346">resetExtensions</a>
</td>
<td align="left" width="63%">
Removes all extensions from the request.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be369059-5852-4cde-8f78-d5883735b670">setPendingRequestInfo</a>
</td>
<td align="left" width="63%">
Sets properties for a pending request.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abcc395f-f989-4098-818a-160e427b1da0">stringToBinary</a>
</td>
<td align="left" width="63%">
Converts an encoded string to a binary data <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICEnroll4</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cde75e0f-5074-44f7-a101-f503913a58f4">CAStoreFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a flag that controls the certificate store when it is opened.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/29616175-7195-430e-a85b-99b50e276e7f">CAStoreName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the name of the store where all non-"ROOT" and non-"MY" certificates are kept.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8b0b113d-4046-4b2b-8f3b-ad08bfe3d0ac">CAStoreType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the type of store to use for the store specified by the 
<a href="https://msdn.microsoft.com/29616175-7195-430e-a85b-99b50e276e7f">CAStoreName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cf46af62-815a-4ad5-bca9-e81eb7c0d1e2">ClientId</a>


</td>
<td align="left" width="10%">


</td>
<td align="left" width="63%">
Sets or retrieves the client ID request attribute.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fa863843-8bbc-47c5-9d58-b64fb6703c0a">ContainerName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the  name of the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key container</a> to use.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f026f4ed-e003-4ece-8c08-427dac48229f">DeleteRequestCert</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a Boolean indicator that controls whether dummy certificates in the request store are deleted.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/057033ab-f2e0-4d60-b47f-73973f82f806">EnableSMIMECapabilities</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that controls whether the PKCS10 will contain a signed <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a> for <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Secure/Multipurpose Internet Mail Extensions</a> (S/MIME) capabilities.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ff8fe103-0303-4f40-af25-efa50155c36f">EnableT61DNEncoding</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that controls whether the distinguished name in the request is encoded as a T61 string instead of as a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">UNICODE</a> string.</p> (Inherited from <a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d22fe4d4-a939-4f77-8e11-f9312c81ec1e">GenKeyFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the values passed to <a href="https://msdn.microsoft.com/b65dd856-2dfa-4cda-9b2f-b32f3c291470">CryptGenKey</a> when the certificate request is generated.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/46f371a3-7254-4f54-b147-402f2a37e277">HashAlgID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the hash algorithm used when signing a PKCS #10 certificate request.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/48f8a47b-0ab4-4150-b8cf-37e57fb04d3e">HashAlgorithm</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves only the signature <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash algorithm</a> used to sign the PKCS #10.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/12150ca2-59cc-402e-b25e-cc98b940ecf8">IncludeSubjectKeyID</a>


</td>
<td align="left" width="10%">


</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that controls whether a subject key identifier extension is included in the certificate request.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/30cc7c86-29ce-42e9-b9dc-d29f5b5450a5">KeySpec</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the  type of key generated.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d8ed3663-bbda-4052-9c72-b00543ca73ab">LimitExchangeKeyToEncipherment</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that controls whether an AT_KEYEXCHANGE request contains <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">digital signature</a> and non-repudiation key usages.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0616c666-9cfc-48f9-93a2-91d51d8dff04">MyStoreFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets the registry location used for the MY store.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/aa08e88d-bd1f-4bd6-806e-56f720846623">MyStoreName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the name of the store  where certificates with linked private keys are kept.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/948a9012-b2ac-4bf0-8cae-690ea3ecdb2e">MyStoreType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the type of store  specified by the 
<a href="https://msdn.microsoft.com/aa08e88d-bd1f-4bd6-806e-56f720846623">MyStoreName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c5099bef-2882-4106-a2e6-a144e16993c3">PrivateKeyArchiveCertificate</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the certificate that is used to archive a private key with a PKCS #7 or CMC request.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ddf92921-368f-4769-b2c1-b9d6a94b0fcb">ProviderFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the CSP type.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/092d5ed1-8d03-45d8-bc7a-3e27035f4b2f">ProviderName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the name of the CSP to use.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/90daa97a-350e-4307-80a5-b018cc1f0e86">ProviderType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the type of provider.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3f841bb2-6cfd-4712-bb71-5c3d9d462fab">PVKFileName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the name of the file that will contain exported keys.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/399870f0-69e1-4a21-a7fa-c3de9ee66876">RequestStoreFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the registry location used for the REQUEST store.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03">RequestStoreName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the store that contains the dummy certificate. This dummy certificate, along with the added private keys, remains in the request store  until a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> processes the request and responds with a PKCS #7.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cc0d09bc-3589-454d-a1fe-141af46bc45b">RequestStoreType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the type of store to use for the store specified by the 
<a href="https://msdn.microsoft.com/c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03">RequestStoreName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5a9d5f78-bf88-4e24-9685-7c504f9f2e38">ReuseHardwareKeyIfUnableToGenNew</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that determines the action taken by the 
certificate enrollment control object if an error is encountered when generating a new key.</p> (Inherited from <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bf844047-4f5a-42de-a446-195371c0dbcf">RootStoreFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the registry location used for the ROOT store.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5b686ade-e8ee-4c59-ab90-05088f575acd">RootStoreName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the root store where all intrinsically trusted self-signed <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">ROOT certificates</a> are kept.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/452f89ad-e512-4ac7-816a-c3f97e25350a">RootStoreType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the type of store to use for the store specified by the 
<a href="https://msdn.microsoft.com/5b686ade-e8ee-4c59-ab90-05088f575acd">RootStoreName</a> property.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3e5b8964-f737-407e-b265-fe095bd6f8ad">SignerCertificate</a>


</td>
<td align="left" width="10%">
Write-only

</td>
<td align="left" width="63%">
Sets the signer's certificate.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4ff2f111-31bd-4ed4-a335-2db536477660">SPCFileName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the file to write the resulting base64-encoded PKCS #7 (in <b>BSTR</b> form) as returned from the certification authority.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/58f027c6-fa92-40ac-b41d-89b6fba7455d">ThumbPrint</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of the certificate data.</p> (Inherited from <b>ICEnroll4</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e5115033-bda1-4160-84b3-80c692bf64fb">UseExistingKeySet</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves a Boolean value that indicates whether the existing keys should be used.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cc622f5b-e6d0-48c5-8535-29d6d4b02129">WriteCertToCSP</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that indicates whether a certificate should be written to the CSP.</p> (Inherited from <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8c80f6b9-f5f7-4fa1-9cb5-db19cdc9ec25">WriteCertToUserDS</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that controls whether the certificate is written to the user's Active Directory store.</p> (Inherited from <a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a>)</td>
</tr>
</table> 

