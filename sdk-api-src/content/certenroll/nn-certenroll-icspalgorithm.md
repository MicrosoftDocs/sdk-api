---
UID: NN:certenroll.ICspAlgorithm
title: ICspAlgorithm
author: windows-sdk-content
description: Represents an algorithm implemented by a cryptographic provider.
old-location: security\icspalgorithm.htm
tech.root: seccertenroll
ms.assetid: 08eba616-2e96-40cd-9fda-8549de98c138
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ICspAlgorithm, ICspAlgorithm interface [Security], ICspAlgorithm interface [Security],described, certenroll/ICspAlgorithm, security.icspalgorithm
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
 - ICspAlgorithm
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICspAlgorithm interface


## -description


The <b>ICspAlgorithm</b> interface represents an algorithm implemented by a cryptographic provider. Providers are separate modules that implement encryption, hashing, signing, and key exchange (archival)  algorithms. Similar providers are grouped together in a type. For example, the <a href="https://msdn.microsoft.com/en-us/library/Aa387448(v=VS.85).aspx">PROV_RSA_FULL</a> type identifies providers that typically support the following algorithms. An individual provider can, however,  choose to support fewer or more algorithms than those listed.<ul>
<li>Encryption: RC2, RC4</li>
<li>Hashing: MD5, SHA</li>
<li>Key Exchange: RSA</li>
<li>Signature: RSA</li>
</ul>For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa386983(v=VS.85).aspx">Microsoft Cryptographic Service Providers</a>. 

A collection of <b>ICspAlgorithm</b> objects can be retrieved from an <a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a> object. The <b>ICspInformation</b> object can be initialized from a provider name or type.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspAlgorithm</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICspAlgorithm</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa965586(v=VS.85).aspx">GetAlgorithmOid</a>
</td>
<td align="left" width="63%">
Retrieves the  algorithm <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID).

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

<a href="https://msdn.microsoft.com/en-us/library/Aa375958(v=VS.85).aspx">DefaultLength</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa375959(v=VS.85).aspx">IncrementLength</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa375960(v=VS.85).aspx">LongName</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa375961(v=VS.85).aspx">MaxLength</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa375962(v=VS.85).aspx">MinLength</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa375963(v=VS.85).aspx">Name</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa375964(v=VS.85).aspx">Operations</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa375966(v=VS.85).aspx">Type</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa965588(v=VS.85).aspx">Valid</a>


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




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380245(v=VS.85).aspx">Cryptographic Service Providers</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

