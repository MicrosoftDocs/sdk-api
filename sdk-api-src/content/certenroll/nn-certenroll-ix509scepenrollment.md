---
UID: NN:certenroll.IX509SCEPEnrollment
title: IX509SCEPEnrollment
author: windows-sdk-content
description: X.509 Simple Computer Enrollment Protocol Interface
old-location: security\ix509scepenrollment.htm
old-project: SecCertEnroll
ms.assetid: fcbac911-9e37-4994-bbb6-544b19a92749
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509SCEPEnrollment, IX509SCEPEnrollment interface [Security], IX509SCEPEnrollment interface [Security],described, certenroll/IX509SCEPEnrollment, security.ix509scepenrollment
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.dll
api_name:
 - IX509SCEPEnrollment
product: Windows
targetos: Windows
req.lib: 
req.dll: Certenroll.dll
req.irql: 
---

# IX509SCEPEnrollment interface


## -description


X.509 Simple Computer Enrollment Protocol Interface


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509SCEPEnrollment</b> interface inherits from the <a href="http://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IX509SCEPEnrollment</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509SCEPEnrollment</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b86d6dc3-aa96-45f3-9551-f24c39ea6cbf">CreateRequestMessage</a>
</td>
<td align="left" width="63%">
Create a PKCS10 request message with a challenge password.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/238a837f-4464-49ce-b87a-03abcfc0abea">CreateRetrieveCertificateMessage</a>
</td>
<td align="left" width="63%">
Retrieve a previously issued certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86d031b0-2009-460b-8bed-fe7a0489f22b">CreateRetrievePendingMessage</a>
</td>
<td align="left" width="63%">
Create a message for certificate polling (manual enrollment).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d709dd46-b6ed-4471-a601-e140a139f57e">DeleteRequest</a>
</td>
<td align="left" width="63%">
Delete the any certificates or keys created for the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initialize the instance in preparation for a new request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b6f9e9d-5316-4928-861a-22497e1f5c00">InitializeForPending</a>
</td>
<td align="left" width="63%">
Initialize the instance to prepare to generate a message to either retrieve an issued certificate, or install a response for a previous request by the issuer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4254fdf3-473f-4f22-a08f-13481fd9f779">ProcessResponseMessage</a>
</td>
<td align="left" width="63%">
Process a response message and return the disposition of the message.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509SCEPEnrollment</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9aa3eaad-d661-4e76-86b5-331bddf50700">Certificate</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the certificate for the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7d6802be-c8d7-45ea-8da2-042414ae5e55">CertificateFriendlyName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the friendly name for the certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4fd76b7e-8b19-46da-b352-7668917a6585">FailInfo</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets information when the <a href="https://msdn.microsoft.com/4254fdf3-473f-4f22-a08f-13481fd9f779">ProcessResponseMessage</a> method detects a failed environment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/caa88227-b068-4b3d-9334-c0283153b1ce">OldCertificate</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets an old certificate that a request is intended to replace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/ff554564">Request</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the inner PKCS10 request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fcfed23f-7798-4b56-afcd-65975a2d39bd">ServerCapabilities</a>


</td>
<td align="left" width="10%">
Write-only

</td>
<td align="left" width="63%">
Sets the hash and encryption algorithms to use for the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7d01acc5-158d-4429-a2e8-d179571f9a1c">SignerCertificate</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the signer certificate for the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6c672181-fdfa-4e9c-9e19-2af9d8bf3a03">Silent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets whether to display UI during the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the status of the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f0688ce9-9c20-4726-ae15-69285c3b30f3">TransactionId</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the transaction id for the request.

</td>
</tr>
</table> 

