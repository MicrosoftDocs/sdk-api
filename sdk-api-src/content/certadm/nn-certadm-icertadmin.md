---
UID: NN:certadm.ICertAdmin
title: ICertAdmin
author: windows-sdk-content
description: Provides administration functionality for properly authorized clients.
old-location: security\icertadmin.htm
tech.root: seccrypto
ms.assetid: e906b69b-5574-4dd5-aa30-9c2a67972202
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICertAdmin, ICertAdmin interface [Security], ICertAdmin interface [Security],described, _certsrv_icertadmin, certadm/ICertAdmin, security.icertadmin
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICertAdmin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertAdmin interface


## -description


The <b>ICertAdmin</b> interface
			provides administration functionality for properly authorized clients.

The <b>ICertAdmin</b> interface is used to perform the following tasks:
<ul>
<li>Authorize or deny a certificate request.</li>
<li>Revoke an issued certificate.</li>
<li>Trigger the generation of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL).</li>
<li>Get the current CRL for the server.</li>
<li>Determine whether a certificate is valid.</li>
</ul>When you use the <b>ICertAdmin</b> interface, you have write-only access to request attributes and certificate extensions, but no direct access to other request and certificate properties.

<b>ICertAdmin</b> is defined in Certadm.h. When you create a program, however, use Certsrv.h as the include file. Certadm.dll, on the other hand, provides the implementation of the <b>ICertAdmin</b> interface. The type information for this interface is also in Certadml.dll, which is shipped with the Platform Software Development Kit (SDK).

Administration tasks use DCOM. Code that calls this interface method as defined in an earlier version of Certadm.h will run on Windows-based servers as long as the client and the server are both running the same Windows operating system.

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertAdmin</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICertAdmin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertAdmin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a432fd66-0f80-4fb8-9778-38b240dd6369">DenyRequest</a>
</td>
<td align="left" width="63%">
Denies a certificate request.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bdfc64dd-7446-4c44-997f-fa0086bfbb4f">GetCRL</a>
</td>
<td align="left" width="63%">
Gets a pointer to the current CRL.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/244b121a-76ba-44fd-b15d-f076b722b030">GetRevocationReason</a>
</td>
<td align="left" width="63%">
Returns a value that specifies the reason a certificate was revoked.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b79a726e-5823-468b-869d-382e6fd73b44">ImportCertificate</a>
</td>
<td align="left" width="63%">
Imports a previously issued certificate.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd133c57-a62e-4083-b4fd-7eaf0c9e7606">IsValidCertificate</a>
</td>
<td align="left" width="63%">
Checks the validity of a certificate.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a42cab2d-2309-43f1-8d67-adbc5923ec45">PublishCRL</a>
</td>
<td align="left" width="63%">
Publishes a new CRL.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/610712d9-3661-42ba-9d2f-27862ba8dbd4">ResubmitRequest</a>
</td>
<td align="left" width="63%">
Submits a pended certificate request to the policy module.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d44ff8c1-a248-4e2a-a73f-55fbea9fce03">RevokeCertificate</a>
</td>
<td align="left" width="63%">
Revokes a certificate on a specified date.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d26061da-acc3-45d8-93de-f2d431d350a6">SetCertificateExtension</a>
</td>
<td align="left" width="63%">
Adds a new extension to a certificate to be issued.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/309c53f9-50cf-4c50-bc48-a4f15a8ced18">SetRequestAttributes</a>
</td>
<td align="left" width="63%">
Sets the attributes of a certificate request.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
</table> 

