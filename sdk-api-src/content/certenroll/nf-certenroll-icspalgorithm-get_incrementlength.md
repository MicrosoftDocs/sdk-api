---
UID: NF:certenroll.ICspAlgorithm.get_IncrementLength
title: ICspAlgorithm::get_IncrementLength (certenroll.h)
description: Retrieves a value, in bits, that can be used to determine valid incremental key lengths for algorithms that support multiple key sizes.
helpviewer_keywords: ["ICspAlgorithm interface [Security]","IncrementLength property","ICspAlgorithm.IncrementLength","ICspAlgorithm.get_IncrementLength","ICspAlgorithm::IncrementLength","ICspAlgorithm::get_IncrementLength","IncrementLength property [Security]","IncrementLength property [Security]","ICspAlgorithm interface","certenroll/ICspAlgorithm::IncrementLength","certenroll/ICspAlgorithm::get_IncrementLength","get_IncrementLength","security.icspalgorithm_incrementlength_property"]
old-location: security\icspalgorithm_incrementlength_property.htm
tech.root: security
ms.assetid: 296ad5b4-d0c1-4fd8-ab55-6ee15b5599b7
ms.date: 12/05/2018
ms.keywords: ICspAlgorithm interface [Security],IncrementLength property, ICspAlgorithm.IncrementLength, ICspAlgorithm.get_IncrementLength, ICspAlgorithm::IncrementLength, ICspAlgorithm::get_IncrementLength, IncrementLength property [Security], IncrementLength property [Security],ICspAlgorithm interface, certenroll/ICspAlgorithm::IncrementLength, certenroll/ICspAlgorithm::get_IncrementLength, get_IncrementLength, security.icspalgorithm_incrementlength_property
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICspAlgorithm::get_IncrementLength
 - certenroll/ICspAlgorithm::get_IncrementLength
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspAlgorithm.IncrementLength
 - ICspAlgorithm.get_IncrementLength
---

# ICspAlgorithm::get_IncrementLength


## -description

The <b>IncrementLength</b> property retrieves a value, in bits, that can be used to determine valid incremental key lengths for algorithms that support multiple key sizes. This property is web enabled.

This property is read-only.

## -parameters

## -remarks

You can use the value of this property to determine valid key sizes for generated keys. For example, if the minimum key length of a DSA signing key is 512 bits, the maximum length is 1,024 bits, and the increment is 64 bits, valid key sizes include 512, 576, 640 and so in 64 bit increments up to  1,024.

The <a href="/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_defaultlength">DefaultLength</a>, <b>IncrementLength</b>, <a href="/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_maxlength">MaxLength</a>, and <a href="/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_minlength">MinLength</a> properties can vary by algorithm and provider. The following table lists a few algorithms for which multiple key sizes can be set. The list is not inclusive.<table>
<tr>
<th>Algorithm OID</th>
<th>Cryptographic provider</th>
<th>Key length (bits)</th>
</tr>
<tr>
<td>XCN_OID_RSA_RSA(1.2.840.113549.1.1.1)

</td>
<td>
Microsoft Smart Card Key Storage Provider

Microsoft Base Smart Card Crypto Provider

</td>
<td>
Minimum: 1,024

Maximum: 4,096

Default: 1,024

Increment: 512

</td>
</tr>
<tr>
<td>XCN_OID_RSA_RSA(1.2.840.113549.1.1.1)

</td>
<td>
Microsoft Software Key Storage Provider

Microsoft Base Cryptographic Provider v1.0

Microsoft Enhanced Cryptographic Provider v1.0

Microsoft Enhanced RSA and AES Cryptographic Provider

Microsoft RSA Schannel Cryptographic Provider

Microsoft Strong Cryptographic Provider

</td>
<td>
Minimum: 384

Maximum: 16,384

Default: 1,024

Increment: 8

</td>
</tr>
<tr>
<td>XCN_OID_X957_DSA(1.2.840.10040.4.1)

</td>
<td>
Microsoft Software Key Storage Provider

Microsoft Base DSS and Diffie-Hellman Cryptographic Provider

Microsoft Base DSS Cryptographic Provider

Microsoft DH Schannel Cryptographic Provider

Microsoft Enhanced DSS and Diffie-Hellman Cryptographic Provider

</td>
<td>
Minimum: 512

Maximum: 1,024

Default: 1,024

Increment: 64

</td>
</tr>
<tr>
<td>XCN_OID_ANSI_X942_DH(1.2.840.10046.2.1)

</td>
<td>
Diffie-Hellman key exchange algorithm.

</td>
<td>
Minimum: 512

Maximum: 1,024

Default: 1,024

Increment: 64

</td>
</tr>
<tr>
<td>XCN_OID_ANSI_X942_DH(1.2.840.10046.2.1)

</td>
<td>
Microsoft DH Schannel Cryptographic Provider

Microsoft Enhanced DSS and Diffie-Hellman Cryptographic Provider

</td>
<td>
Minimum: 512

Maximum: 4,096

Default: 1,024

Increment: 64

</td>
</tr>
<tr>
<td>XCN_OID_RSA_RC2CBC(1.2.840.113549.3.2)

</td>
<td>
Microsoft Software Key Storage Provider

Microsoft Smart Card Key Storage Provider

Microsoft Base Smart Card Crypto Provider

Microsoft DH Schannel Cryptographic Provider

Microsoft Enhanced Cryptographic Provider v1.0

Microsoft Enhanced DSS and Diffie-Hellman Cryptographic Provider

Microsoft Enhanced RSA and AES Cryptographic Provider

Microsoft RSA Schannel Cryptographic Provider

Microsoft Strong Cryptographic Provider

</td>
<td>
Minimum: 40

Maximum: 128

Default: 128

Increment: 8

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_defaultlength">DefaultLength</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a>