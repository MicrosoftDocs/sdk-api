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


The <b>IX509AttributeArchiveKey</b> interface represents an attribute that contains an encrypted  <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> to be archived by a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a>. The key is attached as an unauthenticated attribute to the primary signature of a CMC request. The hash of the encrypted key is encoded as an authenticated attribute in the CMC request. For more information, see the <a href="https://msdn.microsoft.com/52c92629-4c9e-4996-80a2-30e2212b3009">IX509AttributeArchiveKeyHash</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeArchiveKey</b> interface inherits from <a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>. <b>IX509AttributeArchiveKey</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d6c39eaa-53d1-4cc4-bed3-34c9ef62e9d0">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the encrypted private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44865c22-0eca-4781-962c-a10698a435f4">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the attribute from an <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> object, the certification authority encryption certificate, and the symmetric encryption algorithm <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).

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

<a href="https://msdn.microsoft.com/3230cfbf-5486-4f77-9efe-5bc542e3e096">EncryptedKeyBlob</a>


</td>
<td align="left" width="63%">
Retrieves a byte array that contains the encrypted key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7aef6c1e-c3f1-4124-b397-bf13ca610135">EncryptionAlgorithm</a>


</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of the symmetric encryption algorithm used to encrypt the private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c365a2e0-caff-4c92-aa22-33c165ea672e">EncryptionStrength</a>


</td>
<td align="left" width="63%">
Retrieves an integer that contains the encryption strength of the symmetric algorithm used to encrypt the key. This property is not used.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>



<a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a>
 

 

