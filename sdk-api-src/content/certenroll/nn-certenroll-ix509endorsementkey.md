---
UID: NN:certenroll.IX509EndorsementKey
title: IX509EndorsementKey (certenroll.h)

description: X.509 Endorsement Key Interface
old-location: security\ix509endorsementkey.htm
tech.root: seccertenroll
ms.assetid: 24f063a7-02e3-47cf-89ca-ebc63bf3e2dc

ms.date: 12/05/2018
ms.keywords: IX509EndorsementKey, IX509EndorsementKey interface [Security], IX509EndorsementKey interface [Security],described, certenroll/IX509EndorsementKey, security.ix509endorsementkey
ms.topic: interface
f1_keywords: 
 - "certenroll/IX509EndorsementKey"
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
 - IX509EndorsementKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509EndorsementKey interface


## -description


X.509 Endorsement Key Interface


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EndorsementKey</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IX509EndorsementKey</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509EndorsementKey</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-addcertificate">AddCertificate</a>
</td>
<td align="left" width="63%">
Add an endorsement key certificate to the key storage provider (KSP) that supports endorsement keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-close">Close</a>
</td>
<td align="left" width="63%">
Closes the endorsement key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-exportpublickey">ExportPublicKey</a>
</td>
<td align="left" width="63%">
Exports the endorsement public key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-getcertificatebyindex">GetCertificateByIndex</a>
</td>
<td align="left" width="63%">
Gets the endorsement certificate associated with the endorsement key from the key storage provider for the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-getcertificatecount">GetCertificateCount</a>
</td>
<td align="left" width="63%">
Gets the count of the endorsement certificates in the key storage provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-open">Open</a>
</td>
<td align="left" width="63%">
Opens the endorsement key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-removecertificate">RemoveCertificate</a>
</td>
<td align="left" width="63%">
Removes an endorsement certificate related to the endorsement key from the key storage provider.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EndorsementKey</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-get_length">Length</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The bit length of the endorsement key. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-get_opened">Opened</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-open">Open</a> method has been successfully called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-get_providername">ProviderName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The name of the encryption provider. The default is the Microsoft Platform Crypto Provider.

</td>
</tr>
</table> 

