---
UID: NF:certenroll.ICspAlgorithm.get_MinLength
title: ICspAlgorithm::get_MinLength (certenroll.h)
description: Retrieves the minimum permitted length for a key.
helpviewer_keywords: ["ICspAlgorithm interface [Security]","MinLength property","ICspAlgorithm.MinLength","ICspAlgorithm.get_MinLength","ICspAlgorithm::MinLength","ICspAlgorithm::get_MinLength","MinLength property [Security]","MinLength property [Security]","ICspAlgorithm interface","certenroll/ICspAlgorithm::MinLength","certenroll/ICspAlgorithm::get_MinLength","get_MinLength","security.icspalgorithm_minlength_property"]
old-location: security\icspalgorithm_minlength_property.htm
tech.root: security
ms.assetid: 1df00a2d-4004-4c5d-ab70-5d39ca517ebd
ms.date: 12/05/2018
ms.keywords: ICspAlgorithm interface [Security],MinLength property, ICspAlgorithm.MinLength, ICspAlgorithm.get_MinLength, ICspAlgorithm::MinLength, ICspAlgorithm::get_MinLength, MinLength property [Security], MinLength property [Security],ICspAlgorithm interface, certenroll/ICspAlgorithm::MinLength, certenroll/ICspAlgorithm::get_MinLength, get_MinLength, security.icspalgorithm_minlength_property
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
 - ICspAlgorithm::get_MinLength
 - certenroll/ICspAlgorithm::get_MinLength
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
 - ICspAlgorithm.MinLength
 - ICspAlgorithm.get_MinLength
---

# ICspAlgorithm::get_MinLength


## -description

The <b>MinLength</b> property retrieves the minimum permitted length for a key. This property is web enabled.

This property is read-only.

## -parameters

## -remarks

The <a href="/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_defaultlength">DefaultLength</a>, <a href="/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_incrementlength">IncrementLength</a>, <a href="/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_maxlength">MaxLength</a>, and <b>MinLength</b> properties can vary by algorithm and provider. The following table lists a few example maximum, minimum and default key sizes.<table>
<tr>
<th>Algorithm OID</th>
<th>Cryptographic provider</th>
<th>Key length (bits)</th>
</tr>
<tr>
<td>XCN_OID_OIWSEC_desCBC(1.3.14.3.2.7)

</td>
<td>
Microsoft Base DSS and Diffie-Hellman Cryptographic Provider

Microsoft Enhanced Cryptographic Provider v1.0

Microsoft DH Schannel Cryptographic Provider

Microsoft Enhanced RSA and AES Cryptographic Provider

</td>
<td>
Minimum: 56

Maximum: 56

Default: 56

</td>
</tr>
<tr>
<td>XCN_OID_RSA_DES_EDE3_CBC(1.2.840.113549.3.7)

</td>
<td>
Microsoft Base DSS and Diffie-Hellman Cryptographic Provider

Microsoft Enhanced Cryptographic Provider v1.0

Microsoft DH Schannel Cryptographic Provider

Microsoft Enhanced RSA and AES Cryptographic Provider

Microsoft Exchange Cryptographic Provider v1.0

</td>
<td>
Minimum: 168

Maximum: 168

Default: 168

</td>
</tr>
<tr>
<td>XCN_OID_RSA_RSA(1.2.840.113549.1.1.1)

</td>
<td>
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
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a>