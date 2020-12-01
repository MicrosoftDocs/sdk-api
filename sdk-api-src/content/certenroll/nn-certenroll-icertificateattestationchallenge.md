---
UID: NN:certenroll.ICertificateAttestationChallenge
title: ICertificateAttestationChallenge (certenroll.h)
description: Allows applications to decrypt a key attestation challenge received from a server.
helpviewer_keywords: ["ICertificateAttestationChallenge","ICertificateAttestationChallenge interface [Security]","ICertificateAttestationChallenge interface [Security]","described","certenroll/ICertificateAttestationChallenge","security.icertificateattestationchallenge"]
old-location: security\icertificateattestationchallenge.htm
tech.root: security
ms.assetid: 3b8d3104-5824-4801-9b74-59307e650662
ms.date: 12/05/2018
ms.keywords: ICertificateAttestationChallenge, ICertificateAttestationChallenge interface [Security], ICertificateAttestationChallenge interface [Security],described, certenroll/ICertificateAttestationChallenge, security.icertificateattestationchallenge
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertificateAttestationChallenge
 - certenroll/ICertificateAttestationChallenge
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.dll
api_name:
 - ICertificateAttestationChallenge
---

# ICertificateAttestationChallenge interface


## -description

Allows applications to decrypt a key attestation challenge received from a server.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertificateAttestationChallenge</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertificateAttestationChallenge</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertificateAttestationChallenge</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/certenroll/nf-certenroll-icertificateattestationchallenge-decryptchallenge">DecryptChallenge</a>
</td>
<td align="left" width="63%">
Decrypts the challenge from the <a href="/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) response and creates a re-encrypted response to send to the CA.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/certenroll/nf-certenroll-icertificateattestationchallenge-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initialize using the full <a href="/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) response returned from the CA.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertificateAttestationChallenge</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/certenroll/nf-certenroll-icertificateattestationchallenge-get_requestid">RequestID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the request ID from the <a href="/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) response.

</td>
</tr>
</table>

## -remarks

If the challenge is successfully decrypted, the decrypted secret needs to be sent back to the server so that an attested end entity certificate can be issued.