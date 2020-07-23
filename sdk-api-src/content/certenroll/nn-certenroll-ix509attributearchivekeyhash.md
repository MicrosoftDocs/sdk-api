---
UID: NN:certenroll.IX509AttributeArchiveKeyHash
title: IX509AttributeArchiveKeyHash (certenroll.h)
description: Represents an attribute that contains a SHA-1 hash of the encrypted private key to be archived by a certification authority.
helpviewer_keywords: ["IX509AttributeArchiveKeyHash","IX509AttributeArchiveKeyHash interface [Security]","IX509AttributeArchiveKeyHash interface [Security]","described","certenroll/IX509AttributeArchiveKeyHash","security.ix509attributearchivekeyhash"]
old-location: security\ix509attributearchivekeyhash.htm
tech.root: security
ms.assetid: 52c92629-4c9e-4996-80a2-30e2212b3009
ms.date: 12/05/2018
ms.keywords: IX509AttributeArchiveKeyHash, IX509AttributeArchiveKeyHash interface [Security], IX509AttributeArchiveKeyHash interface [Security],described, certenroll/IX509AttributeArchiveKeyHash, security.ix509attributearchivekeyhash
f1_keywords:
- certenroll/IX509AttributeArchiveKeyHash
dev_langs:
- c++
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- CertEnroll.dll
api_name:
- IX509AttributeArchiveKeyHash
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509AttributeArchiveKeyHash interface


## -description


The <b>IX509AttributeArchiveKeyHash</b> interface represents an attribute that contains a SHA-1 <a href="https://docs.microsoft.com/windows/desktop/SecGloss/h-gly">hash</a> of the encrypted  <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">private key</a> to be archived by a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a>. The encrypted key is attached as an unauthenticated attribute to the primary signature of a CMC request. The hash of the encrypted key is encoded as an authenticated attribute in a CMC request.

When a certification authority receives the request, it hashes the unsigned encrypted key and compares it to the signed hash sent by the requester. If the hashes match, the key was not tampered with.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeArchiveKeyHash</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>. <b>IX509AttributeArchiveKeyHash</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509AttributeArchiveKeyHash</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekeyhash-initializedecode">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded byte array that contains a SHA-1 hash of  encrypted private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekeyhash-initializeencodefromencryptedkeyblob">InitializeEncodeFromEncryptedKeyBlob</a>
</td>
<td align="left" width="63%">
Initializes the attribute from an encrypted private key.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeArchiveKeyHash</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekeyhash-get_encryptedkeyhashblob">EncryptedKeyHashBlob</a>


</td>
<td align="left" width="63%">
Retrieves a string that contains a hash of the encrypted private key.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>
 

 

