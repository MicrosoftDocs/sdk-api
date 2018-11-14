---
UID: NN:certenroll.ICertificateAttestationChallenge
title: ICertificateAttestationChallenge
author: windows-sdk-content
description: Allows applications to decrypt a key attestation challenge received from a server.
old-location: security\icertificateattestationchallenge.htm
tech.root: SecCertEnroll
ms.assetid: 3b8d3104-5824-4801-9b74-59307e650662
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICertificateAttestationChallenge, ICertificateAttestationChallenge interface [Security], ICertificateAttestationChallenge interface [Security],described, certenroll/ICertificateAttestationChallenge, security.icertificateattestationchallenge
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICertificateAttestationChallenge
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertificateAttestationChallenge interface


## -description


Allows applications to decrypt a key attestation challenge received from a server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertificateAttestationChallenge</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICertificateAttestationChallenge</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dn379340(v=VS.85).aspx">DecryptChallenge</a>
</td>
<td align="left" width="63%">
Decrypts the challenge from the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">Certificate Management over CMS</a> (CMC) response and creates a re-encrypted response to send to the CA.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn379341(v=VS.85).aspx">Initialize</a>
</td>
<td align="left" width="63%">
Initialize using the full <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">Certificate Management over CMS</a> (CMC) response returned from the CA.

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

<a href="https://msdn.microsoft.com/en-us/library/Dn379344(v=VS.85).aspx">RequestID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the request ID from the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">Certificate Management over CMS</a> (CMC) response.

</td>
</tr>
</table> 


## -remarks



If the challenge is successfully decrypted, the decrypted secret needs to be sent back to the server so that an attested end entity certificate can be issued.



