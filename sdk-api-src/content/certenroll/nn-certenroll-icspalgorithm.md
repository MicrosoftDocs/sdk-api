---
UID: NN:certenroll.ICspAlgorithm
title: ICspAlgorithm (certenroll.h)
author: windows-sdk-content
description: Represents an algorithm implemented by a cryptographic provider.
old-location: security\icspalgorithm.htm
tech.root: seccertenroll
ms.assetid: 08eba616-2e96-40cd-9fda-8549de98c138
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICspAlgorithm, ICspAlgorithm interface [Security], ICspAlgorithm interface [Security],described, certenroll/ICspAlgorithm, security.icspalgorithm
ms.topic: interface
f1_keywords: 
 - "certenroll/ICspAlgorithm"
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
 - ICspAlgorithm
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICspAlgorithm interface


## -description


The <b>ICspAlgorithm</b> interface represents an algorithm implemented by a cryptographic provider. Providers are separate modules that implement encryption, hashing, signing, and key exchange (archival)  algorithms. Similar providers are grouped together in a type. For example, the <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/prov-rsa-full">PROV_RSA_FULL</a> type identifies providers that typically support the following algorithms. An individual provider can, however,  choose to support fewer or more algorithms than those listed.<ul>
<li>Encryption: RC2, RC4</li>
<li>Hashing: MD5, SHA</li>
<li>Key Exchange: RSA</li>
<li>Signature: RSA</li>
</ul>For more information, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/microsoft-cryptographic-service-providers">Microsoft Cryptographic Service Providers</a>. 

A collection of <b>ICspAlgorithm</b> objects can be retrieved from an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> object. The <b>ICspInformation</b> object can be initialized from a provider name or type.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspAlgorithm</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICspAlgorithm</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-getalgorithmoid">GetAlgorithmOid</a>
</td>
<td align="left" width="63%">
Retrieves the  algorithm <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).

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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_defaultlength">DefaultLength</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_incrementlength">IncrementLength</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_longname">LongName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_maxlength">MaxLength</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_minlength">MinLength</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_name">Name</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_operations">Operations</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_type">Type</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_valid">Valid</a>


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




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptographic-service-providers">Cryptographic Service Providers</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

