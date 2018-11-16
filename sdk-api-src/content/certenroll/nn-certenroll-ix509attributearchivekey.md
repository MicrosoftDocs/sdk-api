---
UID: NN:certenroll.IX509AttributeArchiveKey
title: IX509AttributeArchiveKey
author: windows-sdk-content
description: Represents an attribute that contains an encrypted private key to be archived by a certification authority.
old-location: security\ix509attributearchivekey.htm
tech.root: SecCertEnroll
ms.assetid: b42111e9-e39e-4192-9aba-47403fb627dc
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IX509AttributeArchiveKey, IX509AttributeArchiveKey interface [Security], IX509AttributeArchiveKey interface [Security],described, certenroll/IX509AttributeArchiveKey, security.ix509attributearchivekey
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# IX509AttributeArchiveKey interface


## -description


The <b>IX509AttributeArchiveKey</b> interface represents an attribute that contains an encrypted  <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a> to be archived by a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a>. The key is attached as an unauthenticated attribute to the primary signature of a CMC request. The hash of the encrypted key is encoded as an authenticated attribute in the CMC request. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa377060(v=VS.85).aspx">IX509AttributeArchiveKeyHash</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeArchiveKey</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>. <b>IX509AttributeArchiveKey</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa377069(v=VS.85).aspx">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the encrypted private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377070(v=VS.85).aspx">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the attribute from an <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> object, the certification authority encryption certificate, and the symmetric encryption algorithm <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID).

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

<a href="https://msdn.microsoft.com/en-us/library/Aa377066(v=VS.85).aspx">EncryptedKeyBlob</a>


</td>
<td align="left" width="63%">
Retrieves a byte array that contains the encrypted key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377067(v=VS.85).aspx">EncryptionAlgorithm</a>


</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) of the symmetric encryption algorithm used to encrypt the private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377068(v=VS.85).aspx">EncryptionStrength</a>


</td>
<td align="left" width="63%">
Retrieves an integer that contains the encryption strength of the symmetric algorithm used to encrypt the key. This property is not used.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377108(v=VS.85).aspx">IX509Attributes</a>
 

 

