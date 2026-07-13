---
UID: NE:certenroll.AlgorithmOperationFlags
title: AlgorithmOperationFlags (certenroll.h)
description: Specifies the operations that an algorithm can perform.
helpviewer_keywords: ["AlgorithmOperationFlags","AlgorithmOperationFlags enumeration [Security]","XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION","XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION","XCN_NCRYPT_CIPHER_OPERATION","XCN_NCRYPT_EXACT_MATCH_OPERATION","XCN_NCRYPT_HASH_OPERATION","XCN_NCRYPT_NO_OPERATION","XCN_NCRYPT_PREFERENCE_MASK_OPERATION","XCN_NCRYPT_PREFER_NON_SIGNATURE_OPERATION","XCN_NCRYPT_PREFER_SIGNATURE_ONLY_OPERATION","XCN_NCRYPT_RNG_OPERATION","XCN_NCRYPT_SECRET_AGREEMENT_OPERATION","XCN_NCRYPT_SIGNATURE_OPERATION","certenroll/AlgorithmOperationFlags","certenroll/XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION","certenroll/XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION","certenroll/XCN_NCRYPT_CIPHER_OPERATION","certenroll/XCN_NCRYPT_EXACT_MATCH_OPERATION","certenroll/XCN_NCRYPT_HASH_OPERATION","certenroll/XCN_NCRYPT_NO_OPERATION","certenroll/XCN_NCRYPT_PREFERENCE_MASK_OPERATION","certenroll/XCN_NCRYPT_PREFER_NON_SIGNATURE_OPERATION","certenroll/XCN_NCRYPT_PREFER_SIGNATURE_ONLY_OPERATION","certenroll/XCN_NCRYPT_RNG_OPERATION","certenroll/XCN_NCRYPT_SECRET_AGREEMENT_OPERATION","certenroll/XCN_NCRYPT_SIGNATURE_OPERATION","security.algorithmoperationflags_enum"]
old-location: security\algorithmoperationflags_enum.htm
tech.root: security
ms.assetid: 5fa7ee1e-f5ab-44c9-8ae4-a2940f0c6289
ms.date: 12/05/2018
ms.keywords: AlgorithmOperationFlags, AlgorithmOperationFlags enumeration [Security], XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION, XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION, XCN_NCRYPT_CIPHER_OPERATION, XCN_NCRYPT_EXACT_MATCH_OPERATION, XCN_NCRYPT_HASH_OPERATION, XCN_NCRYPT_NO_OPERATION, XCN_NCRYPT_PREFERENCE_MASK_OPERATION, XCN_NCRYPT_PREFER_NON_SIGNATURE_OPERATION, XCN_NCRYPT_PREFER_SIGNATURE_ONLY_OPERATION, XCN_NCRYPT_RNG_OPERATION, XCN_NCRYPT_SECRET_AGREEMENT_OPERATION, XCN_NCRYPT_SIGNATURE_OPERATION, certenroll/AlgorithmOperationFlags, certenroll/XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION, certenroll/XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION, certenroll/XCN_NCRYPT_CIPHER_OPERATION, certenroll/XCN_NCRYPT_EXACT_MATCH_OPERATION, certenroll/XCN_NCRYPT_HASH_OPERATION, certenroll/XCN_NCRYPT_NO_OPERATION, certenroll/XCN_NCRYPT_PREFERENCE_MASK_OPERATION, certenroll/XCN_NCRYPT_PREFER_NON_SIGNATURE_OPERATION, certenroll/XCN_NCRYPT_PREFER_SIGNATURE_ONLY_OPERATION, certenroll/XCN_NCRYPT_RNG_OPERATION, certenroll/XCN_NCRYPT_SECRET_AGREEMENT_OPERATION, certenroll/XCN_NCRYPT_SIGNATURE_OPERATION, security.algorithmoperationflags_enum
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AlgorithmOperationFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AlgorithmOperationFlags
 - certenroll/AlgorithmOperationFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - AlgorithmOperationFlags
---

# AlgorithmOperationFlags enumeration


## -description

The <b>AlgorithmOperationFlags</b> enumeration type specifies the operations that an algorithm can perform. This enumeration is used in the following interfaces to retrieve the operational capabilities of a cryptographic provider or status information based on those capabilities.<ul>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a>
</li>
</ul>


The binary format of the flags are as follows.

``` syntax
XCN_NCRYPT_NO_OPERATION                     = 00000000 00000000 00000000
XCN_NCRYPT_CIPHER_OPERATION                 = 00000000 00000000 00000001
XCN_NCRYPT_HASH_OPERATION                   = 00000000 00000000 00000010

XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION  = 00000000 00000000 00000100
XCN_NCRYPT_SECRET_AGREEMENT_OPERATION       = 00000000 00000000 00001000
XCN_NCRYPT_SIGNATURE_OPERATION              = 00000000 00000000 00010000
XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION         = 00000000 00000000 00011100

XCN_NCRYPT_RNG_OPERATION                    = 00000000 00000000 00100000

XCN_NCRYPT_PREFER_SIGNATURE_ONLY_OPERATION  = 00100000 00000000 00000000
XCN_NCRYPT_PREFER_NON_SIGNATURE_OPERATION   = 01000000 00000000 00000000
XCN_NCRYPT_EXACT_MATCH_OPERATION            = 10000000 00000000 00000000
XCN_NCRYPT_PREFERENCE_MASK_OPERATION        = 11100000 00000000 00000000

```


## -enum-fields

### -field XCN_NCRYPT_NO_OPERATION:0

No operation is specified.

### -field XCN_NCRYPT_CIPHER_OPERATION:0x1

The algorithm can be  used for <a href="/windows/desktop/SecGloss/s-gly">symmetric encryption</a>. This includes the <a href="/windows/desktop/SecGloss/r-gly">RC2</a>, <a href="/windows/desktop/SecGloss/r-gly">RC4</a>, <a href="/windows/desktop/SecGloss/d-gly">Data Encryption Standard</a> (DES), 3DED, and <a href="/windows/desktop/SecGloss/a-gly">AES</a> algorithms.

### -field XCN_NCRYPT_HASH_OPERATION:0x2

The algorithm can be used for hashing. This includes the <a href="/windows/desktop/SecGloss/m-gly">MD2</a>, <a href="/windows/desktop/SecGloss/m-gly">MD4</a>, SHA1, SHA256, SHA384, SHA512 MAC, and <a href="/windows/desktop/SecGloss/h-gly">Hash-Based Message Authentication Code</a> (HMAC) <a href="/windows/desktop/SecGloss/h-gly">hashing algorithms</a>.

### -field XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION:0x4

The algorithm can be used for <a href="/windows/desktop/SecGloss/p-gly">public key</a> encryption. This includes <a href="/windows/desktop/SecGloss/r-gly">RSA</a>.

### -field XCN_NCRYPT_SECRET_AGREEMENT_OPERATION:0x8

The algorithm can used for key exchange. This includes the <a href="/windows/desktop/SecGloss/d-gly">Diffie-Hellman algorithm</a> and ECDH algorithm.

### -field XCN_NCRYPT_SIGNATURE_OPERATION:0x10

The algorithm can be  used for signing. This includes the RSA algorithm, <a href="/windows/desktop/SecGloss/d-gly">Digital Signature Algorithm</a> (DSA), and ECDSA algorithm.

### -field XCN_NCRYPT_RNG_OPERATION:0x20

The algorithm can be used to generate a random number.

### -field XCN_NCRYPT_KEY_DERIVATION_OPERATION:0x40

### -field XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION

The algorithm can be used for public key encryption, key exchange, and signing. This is a bitwise-<b>OR</b> combination of the following constants:

<ul>
<li>XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION</li>
<li>XCN_NCRYPT_SECRET_AGREEMENT_OPERATION</li>
<li>XCN_NCRYPT_SIGNATURE_OPERATION</li>
</ul>

### -field XCN_NCRYPT_PREFER_SIGNATURE_ONLY_OPERATION:0x200000

Signature algorithms are preferred but not required. An encryption algorithm may be chosen instead. This is used when searching for <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) status information based on supported operational capability.

### -field XCN_NCRYPT_PREFER_NON_SIGNATURE_OPERATION:0x400000

An encryption algorithm (such as that identified by the <b>XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION</b> or <b>XCN_NCRYPT_SECRET_AGREEMENT_OPERATION</b> flags) is preferred but not required. A signature algorithm may be chosen instead. This is used when searching for CSP status information based on supported operational capability.

### -field XCN_NCRYPT_EXACT_MATCH_OPERATION:0x800000

Only an algorithm that exactly matches the specified operations is selected.

### -field XCN_NCRYPT_PREFERENCE_MASK_OPERATION:0xe00000

Use to mask the algorithm operation preference.

## -see-also

<a href="/windows/desktop/api/certenroll/ne-certenroll-algorithmtype">AlgorithmType</a>



<a href="/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>
