---
UID: NN:certenroll.IX509SCEPEnrollment
title: IX509SCEPEnrollment
author: windows-sdk-content
description: X.509 Simple Computer Enrollment Protocol Interface
old-location: security\ix509scepenrollment.htm
tech.root: SecCertEnroll
ms.assetid: fcbac911-9e37-4994-bbb6-544b19a92749
ms.author: windowssdkdev
ms.date: 09/26/2018
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
req.lib: 
req.dll: Certenroll.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# IX509SCEPEnrollment interface


## -description


X.509 Simple Computer Enrollment Protocol Interface


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509SCEPEnrollment</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IX509SCEPEnrollment</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dn424976(v=VS.85).aspx">CreateRequestMessage</a>
</td>
<td align="left" width="63%">
Create a PKCS10 request message with a challenge password.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn424977(v=VS.85).aspx">CreateRetrieveCertificateMessage</a>
</td>
<td align="left" width="63%">
Retrieve a previously issued certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn424978(v=VS.85).aspx">CreateRetrievePendingMessage</a>
</td>
<td align="left" width="63%">
Create a message for certificate polling (manual enrollment).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn424979(v=VS.85).aspx">DeleteRequest</a>
</td>
<td align="left" width="63%">
Delete the any certificates or keys created for the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn424981(v=VS.85).aspx">Initialize</a>
</td>
<td align="left" width="63%">
Initialize the instance in preparation for a new request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn424982(v=VS.85).aspx">InitializeForPending</a>
</td>
<td align="left" width="63%">
Initialize the instance to prepare to generate a message to either retrieve an issued certificate, or install a response for a previous request by the issuer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn424985(v=VS.85).aspx">ProcessResponseMessage</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Dn424974(v=VS.85).aspx">Certificate</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Dn424975(v=VS.85).aspx">CertificateFriendlyName</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Dn424980(v=VS.85).aspx">FailInfo</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets information when the <a href="https://msdn.microsoft.com/en-us/library/Dn424985(v=VS.85).aspx">ProcessResponseMessage</a> method detects a failed environment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Dn424984(v=VS.85).aspx">OldCertificate</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Dn424987(v=VS.85).aspx">Request</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Dn424988(v=VS.85).aspx">ServerCapabilities</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Dn424989(v=VS.85).aspx">SignerCertificate</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Dn424990(v=VS.85).aspx">Silent</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Dn424991(v=VS.85).aspx">Status</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Dn424992(v=VS.85).aspx">TransactionId</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the transaction id for the request.

</td>
</tr>
</table> 

