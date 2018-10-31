---
UID: NN:certadm.ICertAdmin2
title: ICertAdmin2
author: windows-sdk-content
description: Provide administration functionality for properly authorized clients.
old-location: security\icertadmin2.htm
tech.root: seccrypto
ms.assetid: df40b6ac-825d-4e8d-a80b-6e57a4e740a2
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ICertAdmin2, ICertAdmin2 interface [Security], ICertAdmin2 interface [Security],described, _certsrv_icertadmin2, certadm/ICertAdmin2, security.icertadmin2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certadm.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertAdmin2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertAdmin2 interface


## -description


The <b>ICertAdmin2</b> interface
			is one of two interfaces that provide administration functionality for properly authorized clients.

The <b>ICertAdmin2</b> interface is used to perform the following tasks:
<ul>
<li>Authorize or deny a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>.</li>
<li>Revoke an issued certificate.</li>
<li>Trigger the generation of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL).</li>
<li>Get the current CRL for the server.</li>
<li>Determine whether a certificate is valid.</li>
<li>Get an archived key.</li>
<li>Get a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) display name, property, or property flag.</li>
<li>Publish one or several CRLs.</li>
<li>Get or set configuration information.</li>
<li>Determine which roles are set.</li>
<li>Import a certificate or key.</li>
</ul>Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertAdmin2</b> interface inherits from <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a> and <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>. <b>ICertAdmin2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertAdmin2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee64740a-850b-4af5-a7cd-75eaa1687f8d">DeleteRow</a>
</td>
<td align="left" width="63%">
Deletes a row, or set of rows, from a database table.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a432fd66-0f80-4fb8-9778-38b240dd6369">DenyRequest</a>
</td>
<td align="left" width="63%">
Denies a certificate request.</p> (Inherited from <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2da85485-99ef-4381-888b-f0ac930b70dc">GetArchivedKey</a>
</td>
<td align="left" width="63%">
Retrieves an archived key recovery <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8eaa2e36-4358-4abd-a7c2-2c9768766597">GetCAProperty</a>
</td>
<td align="left" width="63%">
Retrieves a property value from the CA.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f879b94-d15a-48e6-9e71-a24c1c39c618">GetCAPropertyDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name for a property.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f38bea1-e278-4085-b321-05f6765cc676">GetCAPropertyFlags</a>
</td>
<td align="left" width="63%">
Retrieves the property flags (denoting data type and indexed status) for a property.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1acb9e06-c9e5-419a-899a-b0ae80fab99e">GetConfigEntry</a>
</td>
<td align="left" width="63%">
Retrieves configuration  information for a CA.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bdfc64dd-7446-4c44-997f-fa0086bfbb4f">GetCRL</a>
</td>
<td align="left" width="63%">
Gets a pointer to the current CRL.</p> (Inherited from <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1378f1ad-1e01-4f09-869c-f450b9b2f454">GetMyRoles</a>
</td>
<td align="left" width="63%">
Retrieves the CA roles of the caller.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/244b121a-76ba-44fd-b15d-f076b722b030">GetRevocationReason</a>
</td>
<td align="left" width="63%">
Returns a value that specifies the reason a certificate was revoked.</p> (Inherited from <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b79a726e-5823-468b-869d-382e6fd73b44">ImportCertificate</a>
</td>
<td align="left" width="63%">
Imports a previously issued certificate.</p> (Inherited from <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d71f20d7-5b27-41e5-adc1-6f0ae4160210">ImportKey</a>
</td>
<td align="left" width="63%">
Adds an encrypted key set to an item in the Certificate Services database. The  key set is encrypted to one or several key recovery agent (KRA) certificates.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd133c57-a62e-4083-b4fd-7eaf0c9e7606">IsValidCertificate</a>
</td>
<td align="left" width="63%">
Checks the validity of a certificate.</p> (Inherited from <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a42cab2d-2309-43f1-8d67-adbc5923ec45">PublishCRL</a>
</td>
<td align="left" width="63%">
Publishes a new CRL.</p> (Inherited from <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27f9e991-bf2a-47f3-8f95-b56092fed7d0">PublishCRLs</a>
</td>
<td align="left" width="63%">
Publishes CRLs for the CA.</p> (Inherited from <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/610712d9-3661-42ba-9d2f-27862ba8dbd4">ResubmitRequest</a>
</td>
<td align="left" width="63%">
Submits a pended certificate request to the policy module.</p> (Inherited from <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d44ff8c1-a248-4e2a-a73f-55fbea9fce03">RevokeCertificate</a>
</td>
<td align="left" width="63%">
Revokes a certificate on a specified date.</p> (Inherited from <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29570a8f-41d4-4c6a-88d0-97d6aa9d0784">SetCAProperty</a>
</td>
<td align="left" width="63%">
Sets a property value for the CA.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d26061da-acc3-45d8-93de-f2d431d350a6">SetCertificateExtension</a>
</td>
<td align="left" width="63%">
Adds a new extension to a certificate to be issued.</p> (Inherited from <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ed1dd69-3553-4dcc-a98a-1954013082cd">SetConfigEntry</a>
</td>
<td align="left" width="63%">
Sets configuration  information for a CA.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/309c53f9-50cf-4c50-bc48-a4f15a8ced18">SetRequestAttributes</a>
</td>
<td align="left" width="63%">
Sets the attributes of a certificate request.</p> (Inherited from <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
</table> 

