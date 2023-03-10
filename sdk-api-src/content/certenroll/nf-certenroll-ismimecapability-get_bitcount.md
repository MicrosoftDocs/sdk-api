---
UID: NF:certenroll.ISmimeCapability.get_BitCount
title: ISmimeCapability::get_BitCount (certenroll.h)
description: Retrieves the length, in bits, of the encryption key.
helpviewer_keywords: ["BitCount property [Security]","BitCount property [Security]","ISmimeCapability interface","ISmimeCapability interface [Security]","BitCount property","ISmimeCapability.BitCount","ISmimeCapability.get_BitCount","ISmimeCapability::BitCount","ISmimeCapability::get_BitCount","certenroll/ISmimeCapability::BitCount","certenroll/ISmimeCapability::get_BitCount","get_BitCount","security.ismimecapability_bitcount_property"]
old-location: security\ismimecapability_bitcount_property.htm
tech.root: security
ms.assetid: 582f5d85-9045-4c6f-a4c0-869e6f9e9b9e
ms.date: 12/05/2018
ms.keywords: BitCount property [Security], BitCount property [Security],ISmimeCapability interface, ISmimeCapability interface [Security],BitCount property, ISmimeCapability.BitCount, ISmimeCapability.get_BitCount, ISmimeCapability::BitCount, ISmimeCapability::get_BitCount, certenroll/ISmimeCapability::BitCount, certenroll/ISmimeCapability::get_BitCount, get_BitCount, security.ismimecapability_bitcount_property
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
 - ISmimeCapability::get_BitCount
 - certenroll/ISmimeCapability::get_BitCount
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
 - ISmimeCapability.BitCount
 - ISmimeCapability.get_BitCount
---

# ISmimeCapability::get_BitCount


## -description

The <b>BitCount</b> property retrieves the length, in bits, of the encryption key.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ismimecapability-initialize">Initialize</a> method to specify the <b>BitCount</b> property. The following symmetric encryption algorithms and key lengths are supported by the Certificate Enrollment API.<table>
<tr>
<th>OID</th>
<th>Key Length</th>
</tr>
<tr>
<td>XCN_OID_OIWSEC_desCBC1.3.14.3.2.7

</td>
<td>56</td>
</tr>
<tr>
<td>XCN_OID_RSA_DES_EDE3_CBC1.2.840.113549.3.7

</td>
<td>168</td>
</tr>
<tr>
<td>XCN_OID_RSA_RC2CBC1.2.840.113549.3.2

</td>
<td>40 to 128</td>
</tr>
<tr>
<td>XCN_OID_RSA_RC41.2.840.113549.3.4

</td>
<td>40 to 128</td>
</tr>
<tr>
<td>XCN_OID_RSA_SMIMEalgCMS3DESwrap1.2.840.113549.1.9.16.3.6

</td>
<td>168</td>
</tr>
<tr>
<td>XCN_OID_RSA_SMIMEalgCMSRC2wrap1.2.840.113549.1.9.16.3.7

</td>
<td>128</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES128_CBC2.16.840.1.101.3.4.1.2

</td>
<td>128</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES192_CBC2.16.840.1.101.3.4.1.22

</td>
<td>192</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES256_CBC2.16.840.1.101.3.4.1.42

</td>
<td>256</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES128_WRAP2.16.840.1.101.3.4.1.5

</td>
<td>128</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES192_WRAP2.16.840.1.101.3.4.1.25

</td>
<td>192</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES256_WRAP2.16.840.1.101.3.4.1.45

</td>
<td>256</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapabilities">ISmimeCapabilities</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsmimecapabilities">IX509ExtensionSmimeCapabilities</a>