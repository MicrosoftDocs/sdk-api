---
UID: NN:certenroll.IX509AttributeArchiveKeyHash
title: IX509AttributeArchiveKeyHash
author: windows-sdk-content
description: Represents an attribute that contains a SHA-1 hash of the encrypted private key to be archived by a certification authority.
old-location: security\ix509attributearchivekeyhash.htm
tech.root: SecCertEnroll
ms.assetid: 52c92629-4c9e-4996-80a2-30e2212b3009
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509AttributeArchiveKeyHash, IX509AttributeArchiveKeyHash interface [Security], IX509AttributeArchiveKeyHash interface [Security],described, certenroll/IX509AttributeArchiveKeyHash, security.ix509attributearchivekeyhash
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
 - IX509AttributeArchiveKeyHash
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509AttributeArchiveKeyHash interface


## -description


The <b>IX509AttributeArchiveKeyHash</b> interface represents an attribute that contains a SHA-1 <a href="https://msdn.microsoft.com/en-us/library/ms721586(v=VS.85).aspx">hash</a> of the encrypted  <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a> to be archived by a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a>. The encrypted key is attached as an unauthenticated attribute to the primary signature of a CMC request. The hash of the encrypted key is encoded as an authenticated attribute in a CMC request.

When a certification authority receives the request, it hashes the unsigned encrypted key and compares it to the signed hash sent by the requester. If the hashes match, the key was not tampered with.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeArchiveKeyHash</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>. <b>IX509AttributeArchiveKeyHash</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa377062(v=VS.85).aspx">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded byte array that contains a SHA-1 hash of  encrypted private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377063(v=VS.85).aspx">InitializeEncodeFromEncryptedKeyBlob</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa377061(v=VS.85).aspx">EncryptedKeyHashBlob</a>


</td>
<td align="left" width="63%">
Retrieves a string that contains a hash of the encrypted private key.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377108(v=VS.85).aspx">IX509Attributes</a>
 

 

