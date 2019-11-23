---
UID: NN:certenroll.IX509AttributeCspProvider
title: IX509AttributeCspProvider (certenroll.h)

description: Represents an attribute that identifies the cryptographic provider used by the entity requesting the certificate.
old-location: security\ix509attributecspprovider.htm
tech.root: seccertenroll
ms.assetid: 08954c87-f63b-4e1a-91b4-3773e392999b

ms.date: 12/05/2018
ms.keywords: IX509AttributeCspProvider, IX509AttributeCspProvider interface [Security], IX509AttributeCspProvider interface [Security],described, certenroll/IX509AttributeCspProvider, security.ix509attributecspprovider
ms.topic: interface
f1_keywords: 
 - "certenroll/IX509AttributeCspProvider"
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
 - IX509AttributeCspProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509AttributeCspProvider interface


## -description


The <b>IX509AttributeCspProvider</b> interface represents an attribute that identifies the cryptographic provider used by the entity requesting the certificate. Cryptographic providers and key containers are used to generate and store keys and perform encryption, signing, and hashing.

This attribute is automatically placed in the PKCS #10 attribute collection when you call the  <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeCspProvider</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>. <b>IX509AttributeCspProvider</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-initializedecode">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded byte array that contains information about the provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-initializeencode">InitializeEncode</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-get_keyspec">KeySpec</a>


</td>
<td align="left" width="63%">
Retrieves a value that identifies whether the key pair stored by the provider or key container is used for encryption or for signing content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-get_providername">ProviderName</a>


</td>
<td align="left" width="63%">
Retrieves the provider name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-get_signature">Signature</a>


</td>
<td align="left" width="63%">
Retrieves the digital signature on the provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>
 

 

