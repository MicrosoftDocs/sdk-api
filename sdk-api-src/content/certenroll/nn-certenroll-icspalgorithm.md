---
UID: NN:certenroll.ICspAlgorithm
title: ICspAlgorithm
author: windows-driver-content
description: Represents an algorithm implemented by a cryptographic provider.
old-location: security\icspalgorithm.htm
old-project: SecCertEnroll
ms.assetid: 08eba616-2e96-40cd-9fda-8549de98c138
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ICspAlgorithm, ICspAlgorithm interface [Security], ICspAlgorithm interface [Security], described, certenroll/ICspAlgorithm, security.icspalgorithm
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	ICspAlgorithm
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspAlgorithm interface


## -description


The <b>ICspAlgorithm</b> interface represents an algorithm implemented by a cryptographic provider. Providers are separate modules that implement encryption, hashing, signing, and key exchange (archival)  algorithms. Similar providers are grouped together in a type. For example, the <a href="https://msdn.microsoft.com/44b13a96-aba2-4b77-8e66-416aa0bcb8ad">PROV_RSA_FULL</a> type identifies providers that typically support the following algorithms. An individual provider can, however,  choose to support fewer or more algorithms than those listed.<ul>
<li>Encryption: RC2, RC4</li>
<li>Hashing: MD5, SHA</li>
<li>Key Exchange: RSA</li>
<li>Signature: RSA</li>
</ul>For more information, see <a href="https://msdn.microsoft.com/1461914e-5506-4f24-97da-3d2148aafd1c">Microsoft Cryptographic Service Providers</a>. 

A collection of <b>ICspAlgorithm</b> objects can be retrieved from an <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> object. The <b>ICspInformation</b> object can be initialized from a provider name or type.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspAlgorithm</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICspAlgorithm</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICspAlgorithm</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b922154d-0d57-4473-b331-c0082d9e5db5">GetAlgorithmOid</a>
</td>
<td align="left" width="63%">
Retrieves the  algorithm <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).

[WebEnabled]

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspAlgorithm</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/03a487e0-5ba4-4065-86e9-bed667db6ff9">DefaultLength</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the default length of a key.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/296ad5b4-d0c1-4fd8-ab55-6ee15b5599b7">IncrementLength</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value, in bits, that can be used to determine valid incremental key lengths for algorithms that support multiple key sizes.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/aaa5175f-c110-4e76-9145-1c667ea169a1">LongName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the full name of the algorithm.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/516afaa4-0317-4f05-87e7-bd614b428ccb">MaxLength</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the maximum permitted length for a key.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1df00a2d-4004-4c5d-ab70-5d39ca517ebd">MinLength</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the minimum permitted length for a key.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the abbreviated algorithm name.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/46e6bf91-a50a-4360-9bfe-e41e8bcc1112">Operations</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the operations that can be performed by the algorithm.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the algorithm type.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8f8e9f23-f857-49d3-9519-061ccce27514">Valid</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the algorithm object is valid.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/4e6eb2df-a917-4533-b9f1-8da39598d0b8">Cryptographic Service Providers</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

