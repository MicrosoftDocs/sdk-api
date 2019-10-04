---
UID: NN:certenroll.IX509SCEPEnrollment
title: IX509SCEPEnrollment (certenroll.h)
author: windows-sdk-content
description: X.509 Simple Computer Enrollment Protocol Interface
old-location: security\ix509scepenrollment.htm
tech.root: seccertenroll
ms.assetid: fcbac911-9e37-4994-bbb6-544b19a92749
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509SCEPEnrollment, IX509SCEPEnrollment interface [Security], IX509SCEPEnrollment interface [Security],described, certenroll/IX509SCEPEnrollment, security.ix509scepenrollment
ms.topic: interface
f1_keywords: 
 - "certenroll/IX509SCEPEnrollment"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509SCEPEnrollment interface


## -description


X.509 Simple Computer Enrollment Protocol Interface


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509SCEPEnrollment</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IX509SCEPEnrollment</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage">CreateRequestMessage</a>
</td>
<td align="left" width="63%">
Create a PKCS10 request message with a challenge password.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage">CreateRetrieveCertificateMessage</a>
</td>
<td align="left" width="63%">
Retrieve a previously issued certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage">CreateRetrievePendingMessage</a>
</td>
<td align="left" width="63%">
Create a message for certificate polling (manual enrollment).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-deleterequest">DeleteRequest</a>
</td>
<td align="left" width="63%">
Delete the any certificates or keys created for the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initialize the instance in preparation for a new request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-initializeforpending">InitializeForPending</a>
</td>
<td align="left" width="63%">
Initialize the instance to prepare to generate a message to either retrieve an issued certificate, or install a response for a previous request by the issuer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage">ProcessResponseMessage</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-get_certificate">Certificate</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-get_certificatefriendlyname">CertificateFriendlyName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-get_failinfo">FailInfo</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets information when the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage">ProcessResponseMessage</a> method detects a failed environment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-get_oldcertificate">OldCertificate</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-get_request">Request</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-put_servercapabilities">ServerCapabilities</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-get_signercertificate">SignerCertificate</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-put_silent">Silent</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-get_status">Status</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-get_transactionid">TransactionId</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the transaction id for the request.

</td>
</tr>
</table> 

