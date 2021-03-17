---
UID: NF:certenroll.ICspInformation.get_KeySpec
title: ICspInformation::get_KeySpec (certenroll.h)
description: Retrieves a value that specifies the intended use of the algorithms supported by the provider.
helpviewer_keywords: ["ICspInformation interface [Security]","KeySpec property","ICspInformation.KeySpec","ICspInformation.get_KeySpec","ICspInformation::KeySpec","ICspInformation::get_KeySpec","KeySpec property [Security]","KeySpec property [Security]","ICspInformation interface","XCN_AT_KEYEXCHANGE (1)","XCN_AT_SIGNATURE (2)","certenroll/ICspInformation::KeySpec","certenroll/ICspInformation::get_KeySpec","get_KeySpec","security.icspinformation_keyspec_property"]
old-location: security\icspinformation_keyspec_property.htm
tech.root: security
ms.assetid: f66f2f5c-7f50-4be6-973e-844d6cb76f61
ms.date: 12/05/2018
ms.keywords: ICspInformation interface [Security],KeySpec property, ICspInformation.KeySpec, ICspInformation.get_KeySpec, ICspInformation::KeySpec, ICspInformation::get_KeySpec, KeySpec property [Security], KeySpec property [Security],ICspInformation interface, XCN_AT_KEYEXCHANGE (1), XCN_AT_SIGNATURE (2), certenroll/ICspInformation::KeySpec, certenroll/ICspInformation::get_KeySpec, get_KeySpec, security.icspinformation_keyspec_property
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
 - ICspInformation::get_KeySpec
 - certenroll/ICspInformation::get_KeySpec
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
 - ICspInformation.KeySpec
 - ICspInformation.get_KeySpec
---

# ICspInformation::get_KeySpec


## -description

The <b>KeySpec</b> property retrieves a value that specifies the intended use of the algorithms supported by the provider. This property is web enabled.

This property is read-only.

## -parameters

## -remarks

The value retrieved can be 0, 1, 2, or 3. If the value is 0 (XCN_AT_NONE), the provider is a Cryptography API: Next Generation (CNG) provider. The values associated with the providers distributed by Microsoft are listed in the following table. Some of these providers may not be included on all operating systems and others may be included instead.<table>
<tr>
<th>Provider</th>
<th>KeySpec value</th>
</tr>
<tr>
<td>
Microsoft Software Key Storage Provider

</td>
<td>
0

</td>
</tr>
<tr>
<td>
Microsoft Smart Card Key Storage Provider

</td>
<td>
0

</td>
</tr>
<tr>
<td>
Microsoft Base Cryptographic Provider v1.0

</td>
<td>
3

</td>
</tr>
<tr>
<td>
Microsoft Base DSS and Diffie-Hellman Cryptographic Provider

</td>
<td>
3

</td>
</tr>
<tr>
<td>
Microsoft Base DSS Cryptographic Provider

</td>
<td>
2

</td>
</tr>
<tr>
<td>
Microsoft Base Smart Card Crypto Provider

</td>
<td>
3

</td>
</tr>
<tr>
<td>
Microsoft DH Schannel Cryptographic Provider

</td>
<td>
3

</td>
</tr>
<tr>
<td>
Microsoft Enhanced Cryptographic Provider v1.0

</td>
<td>
3

</td>
</tr>
<tr>
<td>
Microsoft Enhanced DSS and Diffie-Hellman Cryptographic Provider

</td>
<td>
3

</td>
</tr>
<tr>
<td>
Microsoft Enhanced RSA and AES Cryptographic Provider

</td>
<td>
3

</td>
</tr>
<tr>
<td>
Microsoft RSA Schannel Cryptographic Provider

</td>
<td>
1

</td>
</tr>
<tr>
<td>
Microsoft Strong Cryptographic Provider

</td>
<td>
3

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>