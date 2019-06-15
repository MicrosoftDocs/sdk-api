---
UID: NN:certenroll.IX509AttributeArchiveKey
title: IX509AttributeArchiveKey (certenroll.h)
author: windows-sdk-content
description: Represents an attribute that contains an encrypted private key to be archived by a certification authority.
old-location: security\ix509attributearchivekey.htm
tech.root: seccertenroll
ms.assetid: b42111e9-e39e-4192-9aba-47403fb627dc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509AttributeArchiveKey, IX509AttributeArchiveKey interface [Security], IX509AttributeArchiveKey interface [Security],described, certenroll/IX509AttributeArchiveKey, security.ix509attributearchivekey
ms.topic: interface
f1_keywords: ["certenroll/IX509AttributeArchiveKey"]
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
 - IX509AttributeArchiveKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509AttributeArchiveKey interface


## -description


The <b>IX509AttributeArchiveKey</b> interface represents an attribute that contains an encrypted  <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">private key</a> to be archived by a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a>. The key is attached as an unauthenticated attribute to the primary signature of a CMC request. The hash of the encrypted key is encoded as an authenticated attribute in the CMC request. For more information, see the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekeyhash">IX509AttributeArchiveKeyHash</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeArchiveKey</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>. <b>IX509AttributeArchiveKey</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509AttributeArchiveKey</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-initializedecode">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the encrypted private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-initializeencode">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the attribute from an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> object, the certification authority encryption certificate, and the symmetric encryption algorithm <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeArchiveKey</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-get_encryptedkeyblob">EncryptedKeyBlob</a>


</td>
<td align="left" width="63%">
Retrieves a byte array that contains the encrypted key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-get_encryptionalgorithm">EncryptionAlgorithm</a>


</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of the symmetric encryption algorithm used to encrypt the private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-get_encryptionstrength">EncryptionStrength</a>


</td>
<td align="left" width="63%">
Retrieves an integer that contains the encryption strength of the symmetric algorithm used to encrypt the key. This property is not used.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>
 

 

