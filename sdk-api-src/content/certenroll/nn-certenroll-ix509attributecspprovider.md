---
UID: NN:certenroll.IX509AttributeCspProvider
title: IX509AttributeCspProvider
author: windows-sdk-content
description: Represents an attribute that identifies the cryptographic provider used by the entity requesting the certificate.
old-location: security\ix509attributecspprovider.htm
tech.root: SecCertEnroll
ms.assetid: 08954c87-f63b-4e1a-91b4-3773e392999b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509AttributeCspProvider, IX509AttributeCspProvider interface [Security], IX509AttributeCspProvider interface [Security],described, certenroll/IX509AttributeCspProvider, security.ix509attributecspprovider
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
 - IX509AttributeCspProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509AttributeCspProvider interface


## -description


The <b>IX509AttributeCspProvider</b> interface represents an attribute that identifies the cryptographic provider used by the entity requesting the certificate. Cryptographic providers and key containers are used to generate and store keys and perform encryption, signing, and hashing.

This attribute is automatically placed in the PKCS #10 attribute collection when you call the  <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeCspProvider</b> interface inherits from <a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>. <b>IX509AttributeCspProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509AttributeCspProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7098ee8d-39e9-4463-97fe-309265c6baa7">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array that contains information about the provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0b45ea2-b682-4065-8624-08c34581b5ea">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the attribute from information about the provider.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeCspProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4bb04097-9e6c-4b15-852e-be86d21637bf">KeySpec</a>


</td>
<td align="left" width="63%">
Retrieves a value that identifies whether the key pair stored by the provider or key container is used for encryption or for signing content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4a62d1e4-4d00-416b-b44a-23a9cbc53a5b">ProviderName</a>


</td>
<td align="left" width="63%">
Retrieves the provider name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/06245293-b331-4963-a0cf-b7c604580908">Signature</a>


</td>
<td align="left" width="63%">
Retrieves the digital signature on the provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>



<a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a>
 

 

