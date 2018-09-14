---
UID: NN:certenroll.IX509AttributeCspProvider
title: IX509AttributeCspProvider
author: windows-sdk-content
description: Represents an attribute that identifies the cryptographic provider used by the entity requesting the certificate.
old-location: security\ix509attributecspprovider.htm
tech.root: seccertenroll
ms.assetid: 08954c87-f63b-4e1a-91b4-3773e392999b
ms.author: windowssdkdev
ms.date: 08/31/2018
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

This attribute is automatically placed in the PKCS #10 attribute collection when you call the  <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeCspProvider</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>. <b>IX509AttributeCspProvider</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa377083(v=VS.85).aspx">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded byte array that contains information about the provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377084(v=VS.85).aspx">InitializeEncode</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa377085(v=VS.85).aspx">KeySpec</a>


</td>
<td align="left" width="63%">
Retrieves a value that identifies whether the key pair stored by the provider or key container is used for encryption or for signing content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377088(v=VS.85).aspx">ProviderName</a>


</td>
<td align="left" width="63%">
Retrieves the provider name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377089(v=VS.85).aspx">Signature</a>


</td>
<td align="left" width="63%">
Retrieves the digital signature on the provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377108(v=VS.85).aspx">IX509Attributes</a>
 

 

