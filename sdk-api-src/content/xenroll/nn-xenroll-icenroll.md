---
UID: NN:xenroll.ICEnroll
title: ICEnroll
author: windows-sdk-content
description: The ICEnroll interface is one of several interfaces that represent the Certificate Enrollment Control.
old-location: security\icenroll.htm
tech.root: SecCrypto
ms.assetid: d5b746e0-91bd-45bd-9a67-ddc8868cee56
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ICEnroll, ICEnroll interface [Security], ICEnroll interface [Security],described, _xen_icenroll, security.icenroll, xenroll/ICEnroll
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
 - ICEnroll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll interface


## -description


<p class="CCE_Message">[This interface is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ICEnroll</b> interface is one of several interfaces that represent the Certificate Enrollment Control. It is primarily of interest if you are not using Automation. If, on the other hand, you are programming in Visual Basic or another Automation language, see the 
<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICEnroll</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICEnroll</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICEnroll</b> interface has these methods.
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
Accepts and processes a file that contains a PKCS #7 message containing a certificate.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a428d83-c846-4f44-a682-58c3e025c353">acceptPKCS7</a>
</td>
<td align="left" width="63%">
Accepts and processes a PKCS #7 message containing a certificate. The PKCS #7 is input as a parameter.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/074c7321-6117-4261-836a-a2055c9e029d">createFilePKCS10</a>
</td>
<td align="left" width="63%">
Creates a base64-encoded PKCS #10 <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a> and saves it in a file.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8e841c1-f16e-4f3a-94f2-ef6708c88910">createPKCS10</a>
</td>
<td align="left" width="63%">
Creates a base64-encoded PKCS #10 certificate request.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28102a55-3bda-4413-84b6-cfa2057be98b">enumContainers</a>
</td>
<td align="left" width="63%">
Retrieves the names of the containers for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) specified by the 
<a href="https://msdn.microsoft.com/092d5ed1-8d03-45d8-bc7a-3e27035f4b2f">ProviderName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05188aee-2b03-46bc-89f4-506a019496a4">enumProviders</a>
</td>
<td align="left" width="63%">
Retrieves the names of the available CSPs specified by the 
<a href="https://msdn.microsoft.com/90daa97a-350e-4307-80a5-b018cc1f0e86">ProviderType</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d3fd4d4-779f-4e28-9b07-4de17262ac5e">freeRequestInfo</a>
</td>
<td align="left" width="63%">
Cleans up the stores if an error occurs. Currently not implemented.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cde75e0f-5074-44f7-a101-f503913a58f4">get_CAStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/cde75e0f-5074-44f7-a101-f503913a58f4">CAStoreFlags</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29616175-7195-430e-a85b-99b50e276e7f">get_CAStoreName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/29616175-7195-430e-a85b-99b50e276e7f">CAStoreName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b0b113d-4046-4b2b-8f3b-ad08bfe3d0ac">get_CAStoreType</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/8b0b113d-4046-4b2b-8f3b-ad08bfe3d0ac">CAStoreType</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa863843-8bbc-47c5-9d58-b64fb6703c0a">get_ContainerName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/fa863843-8bbc-47c5-9d58-b64fb6703c0a">ContainerName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f026f4ed-e003-4ece-8c08-427dac48229f">get_DeleteRequestCert</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/f026f4ed-e003-4ece-8c08-427dac48229f">DeleteRequestCert</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d22fe4d4-a939-4f77-8e11-f9312c81ec1e">get_GenKeyFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/d22fe4d4-a939-4f77-8e11-f9312c81ec1e">GenKeyFlags</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48f8a47b-0ab4-4150-b8cf-37e57fb04d3e">get_HashAlgorithm</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/48f8a47b-0ab4-4150-b8cf-37e57fb04d3e">HashAlgorithm</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30cc7c86-29ce-42e9-b9dc-d29f5b5450a5">get_KeySpec</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/30cc7c86-29ce-42e9-b9dc-d29f5b5450a5">KeySpec</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0616c666-9cfc-48f9-93a2-91d51d8dff04">get_MyStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/0616c666-9cfc-48f9-93a2-91d51d8dff04">MyStoreFlags</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa08e88d-bd1f-4bd6-806e-56f720846623">get_MyStoreName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/aa08e88d-bd1f-4bd6-806e-56f720846623">MyStoreName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/948a9012-b2ac-4bf0-8cae-690ea3ecdb2e">get_MyStoreType</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/948a9012-b2ac-4bf0-8cae-690ea3ecdb2e">MyStoreType</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddf92921-368f-4769-b2c1-b9d6a94b0fcb">get_ProviderFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/ddf92921-368f-4769-b2c1-b9d6a94b0fcb">ProviderFlags</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/092d5ed1-8d03-45d8-bc7a-3e27035f4b2f">get_ProviderName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/092d5ed1-8d03-45d8-bc7a-3e27035f4b2f">ProviderName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90daa97a-350e-4307-80a5-b018cc1f0e86">get_ProviderType</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/90daa97a-350e-4307-80a5-b018cc1f0e86">ProviderType</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f841bb2-6cfd-4712-bb71-5c3d9d462fab">get_PVKFileName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/3f841bb2-6cfd-4712-bb71-5c3d9d462fab">PVKFileName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/399870f0-69e1-4a21-a7fa-c3de9ee66876">get_RequestStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/399870f0-69e1-4a21-a7fa-c3de9ee66876">RequestStoreFlags</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03">get_RequestStoreName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03">RequestStoreName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc0d09bc-3589-454d-a1fe-141af46bc45b">get_RequestStoreType</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/cc0d09bc-3589-454d-a1fe-141af46bc45b">RequestStoreType</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf844047-4f5a-42de-a446-195371c0dbcf">get_RootStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/bf844047-4f5a-42de-a446-195371c0dbcf">RootStoreFlags</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b686ade-e8ee-4c59-ab90-05088f575acd">get_RootStoreName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/5b686ade-e8ee-4c59-ab90-05088f575acd">RootStoreName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/452f89ad-e512-4ac7-816a-c3f97e25350a">get_RootStoreType</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/452f89ad-e512-4ac7-816a-c3f97e25350a">RootStoreType</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ff2f111-31bd-4ed4-a335-2db536477660">get_SPCFileName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/4ff2f111-31bd-4ed4-a335-2db536477660">SPCFileName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5115033-bda1-4160-84b3-80c692bf64fb">get_UseExistingKeySet</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/e5115033-bda1-4160-84b3-80c692bf64fb">UseExistingKeySet</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc622f5b-e6d0-48c5-8535-29d6d4b02129">get_WriteCertToCSP</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://msdn.microsoft.com/cc622f5b-e6d0-48c5-8535-29d6d4b02129">WriteCertToCSP</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3094cd58-d123-40f1-ac81-dffdfb56d47d">getCertFromPKCS7</a>
</td>
<td align="left" width="63%">
Retrieves the certificate, contained in a PKCS #7 message, that was  issued in response to a PKCS #10 certificate request.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0616c666-9cfc-48f9-93a2-91d51d8dff04">put MyStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/0616c666-9cfc-48f9-93a2-91d51d8dff04">MyStoreFlags</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cde75e0f-5074-44f7-a101-f503913a58f4">put_CAStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/cde75e0f-5074-44f7-a101-f503913a58f4">CAStoreFlags</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29616175-7195-430e-a85b-99b50e276e7f">put_CAStoreName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/29616175-7195-430e-a85b-99b50e276e7f">CAStoreName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b0b113d-4046-4b2b-8f3b-ad08bfe3d0ac">put_CAStoreType</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/8b0b113d-4046-4b2b-8f3b-ad08bfe3d0ac">CAStoreType</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa863843-8bbc-47c5-9d58-b64fb6703c0a">put_ContainerName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/fa863843-8bbc-47c5-9d58-b64fb6703c0a">ContainerName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f026f4ed-e003-4ece-8c08-427dac48229f">put_DeleteRequestCert</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/f026f4ed-e003-4ece-8c08-427dac48229f">DeleteRequestCert</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d22fe4d4-a939-4f77-8e11-f9312c81ec1e">put_GenKeyFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/d22fe4d4-a939-4f77-8e11-f9312c81ec1e">GenKeyFlags</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48f8a47b-0ab4-4150-b8cf-37e57fb04d3e">put_HashAlgorithm</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/48f8a47b-0ab4-4150-b8cf-37e57fb04d3e">HashAlgorithm</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30cc7c86-29ce-42e9-b9dc-d29f5b5450a5">put_KeySpec</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/30cc7c86-29ce-42e9-b9dc-d29f5b5450a5">KeySpec</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa08e88d-bd1f-4bd6-806e-56f720846623">put_MyStoreName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/aa08e88d-bd1f-4bd6-806e-56f720846623">MyStoreName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/948a9012-b2ac-4bf0-8cae-690ea3ecdb2e">put_MyStoreType</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/948a9012-b2ac-4bf0-8cae-690ea3ecdb2e">MyStoreType</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddf92921-368f-4769-b2c1-b9d6a94b0fcb">put_ProviderFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/ddf92921-368f-4769-b2c1-b9d6a94b0fcb">ProviderFlags</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/092d5ed1-8d03-45d8-bc7a-3e27035f4b2f">put_ProviderName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/092d5ed1-8d03-45d8-bc7a-3e27035f4b2f">ProviderName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90daa97a-350e-4307-80a5-b018cc1f0e86">put_ProviderType</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/90daa97a-350e-4307-80a5-b018cc1f0e86">ProviderType</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f841bb2-6cfd-4712-bb71-5c3d9d462fab">put_PVKFileName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/3f841bb2-6cfd-4712-bb71-5c3d9d462fab">PVKFileName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/399870f0-69e1-4a21-a7fa-c3de9ee66876">put_RequestStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/399870f0-69e1-4a21-a7fa-c3de9ee66876">RequestStoreFlags</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03">put_RequestStoreName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03">RequestStoreName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc0d09bc-3589-454d-a1fe-141af46bc45b">put_RequestStoreType</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/cc0d09bc-3589-454d-a1fe-141af46bc45b">RequestStoreType</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf844047-4f5a-42de-a446-195371c0dbcf">put_RootStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/bf844047-4f5a-42de-a446-195371c0dbcf">RootStoreFlags</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b686ade-e8ee-4c59-ab90-05088f575acd">put_RootStoreName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/5b686ade-e8ee-4c59-ab90-05088f575acd">RootStoreName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/452f89ad-e512-4ac7-816a-c3f97e25350a">put_RootStoreType</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/452f89ad-e512-4ac7-816a-c3f97e25350a">RootStoreType</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ff2f111-31bd-4ed4-a335-2db536477660">put_SPCFileName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/4ff2f111-31bd-4ed4-a335-2db536477660">SPCFileName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5115033-bda1-4160-84b3-80c692bf64fb">put_UseExistingKeySet</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/e5115033-bda1-4160-84b3-80c692bf64fb">UseExistingKeySet</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc622f5b-e6d0-48c5-8535-29d6d4b02129">put_WriteCertToCSP</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://msdn.microsoft.com/cc622f5b-e6d0-48c5-8535-29d6d4b02129">WriteCertToCSP</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICEnroll</b> interface has these properties.
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
Sets or retrieves a flag that controls the certificate store when it is opened.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/29616175-7195-430e-a85b-99b50e276e7f">CAStoreName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the name of the store where all non-"ROOT" and non-"MY" certificates are kept.</p> (Inherited from <b>ICEnroll</b>)</td>
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
<a href="https://msdn.microsoft.com/29616175-7195-430e-a85b-99b50e276e7f">CAStoreName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fa863843-8bbc-47c5-9d58-b64fb6703c0a">ContainerName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the  name of the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key container</a> to use.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f026f4ed-e003-4ece-8c08-427dac48229f">DeleteRequestCert</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a Boolean indicator that controls whether dummy certificates in the request store are deleted.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d22fe4d4-a939-4f77-8e11-f9312c81ec1e">GenKeyFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a flag that controls whether a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> is exportable.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/48f8a47b-0ab4-4150-b8cf-37e57fb04d3e">HashAlgorithm</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves only the signature <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash algorithm</a> used to sign the PKCS #10.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/30cc7c86-29ce-42e9-b9dc-d29f5b5450a5">KeySpec</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the  type of key generated.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0616c666-9cfc-48f9-93a2-91d51d8dff04">MyStoreFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets the registry location used for the MY store.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/aa08e88d-bd1f-4bd6-806e-56f720846623">MyStoreName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the name of the store  where certificates with linked private keys are kept.</p> (Inherited from <b>ICEnroll</b>)</td>
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
<a href="https://msdn.microsoft.com/aa08e88d-bd1f-4bd6-806e-56f720846623">MyStoreName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ddf92921-368f-4769-b2c1-b9d6a94b0fcb">ProviderFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the CSP type.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/092d5ed1-8d03-45d8-bc7a-3e27035f4b2f">ProviderName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the name of the CSP to use.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/90daa97a-350e-4307-80a5-b018cc1f0e86">ProviderType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the type of provider.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3f841bb2-6cfd-4712-bb71-5c3d9d462fab">PVKFileName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the name of the file that will contain exported keys.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/399870f0-69e1-4a21-a7fa-c3de9ee66876">RequestStoreFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the registry location used for the REQUEST store.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03">RequestStoreName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the store that contains the dummy certificate. This dummy certificate, along with the added private keys, remains in the request store  until a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> processes the request and responds with a PKCS #7. </p> (Inherited from <b>ICEnroll</b>)</td>
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
<a href="https://msdn.microsoft.com/c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03">RequestStoreName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bf844047-4f5a-42de-a446-195371c0dbcf">RootStoreFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the registry location used for the ROOT store.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5b686ade-e8ee-4c59-ab90-05088f575acd">RootStoreName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the root store where all intrinsically trusted self-signed <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">ROOT certificates</a> are kept.</p> (Inherited from <b>ICEnroll</b>)</td>
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
<a href="https://msdn.microsoft.com/5b686ade-e8ee-4c59-ab90-05088f575acd">RootStoreName</a> property.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4ff2f111-31bd-4ed4-a335-2db536477660">SPCFileName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the file to write the resulting base64-encoded PKCS #7 (in <b>BSTR</b> form) as returned from the certification authority.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e5115033-bda1-4160-84b3-80c692bf64fb">UseExistingKeySet</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves a Boolean value that indicates whether the existing keys should be used.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cc622f5b-e6d0-48c5-8535-29d6d4b02129">WriteCertToCSP</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that indicates whether a certificate should be written to the CSP.</p> (Inherited from <b>ICEnroll</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

