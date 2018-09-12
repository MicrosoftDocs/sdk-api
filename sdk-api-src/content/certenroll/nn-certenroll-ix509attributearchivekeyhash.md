---
UID: NN:certenroll.IX509AttributeArchiveKeyHash
title: IX509AttributeArchiveKeyHash
author: windows-sdk-content
description: Represents an attribute that contains a SHA-1 hash of the encrypted private key to be archived by a certification authority.
old-location: security\ix509attributearchivekeyhash.htm
tech.root: SecCertEnroll
ms.assetid: 52c92629-4c9e-4996-80a2-30e2212b3009
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509AttributeArchiveKeyHash, IX509AttributeArchiveKeyHash interface [Security], IX509AttributeArchiveKeyHash interface [Security],described, certenroll/IX509AttributeArchiveKeyHash, security.ix509attributearchivekeyhash
ms.prod: windows
ms.technology: windows-sdk
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


The <b>IX509AttributeArchiveKeyHash</b> interface represents an attribute that contains a SHA-1 <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of the encrypted  <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> to be archived by a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a>. The encrypted key is attached as an unauthenticated attribute to the primary signature of a CMC request. The hash of the encrypted key is encoded as an authenticated attribute in a CMC request.

When a certification authority receives the request, it hashes the unsigned encrypted key and compares it to the signed hash sent by the requester. If the hashes match, the key was not tampered with.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeArchiveKeyHash</b> interface inherits from <a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>. <b>IX509AttributeArchiveKeyHash</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c8f59fba-c6ce-4e11-bb25-8a6fd23218d1">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array that contains a SHA-1 hash of  encrypted private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2101f15f-b71b-4dea-8ec8-2d3c1926ae15">InitializeEncodeFromEncryptedKeyBlob</a>
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

<a href="https://msdn.microsoft.com/ff75aaf8-1544-465b-af0d-620ca6984249">EncryptedKeyHashBlob</a>


</td>
<td align="left" width="63%">
Retrieves a string that contains a hash of the encrypted private key.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>



<a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a>
 

 

