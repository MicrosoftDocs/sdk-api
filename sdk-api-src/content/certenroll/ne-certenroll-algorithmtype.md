---
UID: NE:certenroll.AlgorithmType
title: AlgorithmType (certenroll.h)
description: Specifies the intended purpose of a cryptographic algorithm supported by a cryptographic provider.
helpviewer_keywords: ["AlgorithmType","AlgorithmType enumeration [Security]","XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE","XCN_BCRYPT_CIPHER_INTERFACE","XCN_BCRYPT_HASH_INTERFACE","XCN_BCRYPT_RNG_INTERFACE","XCN_BCRYPT_SECRET_AGREEMENT_INTERFACE","XCN_BCRYPT_SIGNATURE_INTERFACE","XCN_BCRYPT_UNKNOWN_INTERFACE","certenroll/AlgorithmType","certenroll/XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE","certenroll/XCN_BCRYPT_CIPHER_INTERFACE","certenroll/XCN_BCRYPT_HASH_INTERFACE","certenroll/XCN_BCRYPT_RNG_INTERFACE","certenroll/XCN_BCRYPT_SECRET_AGREEMENT_INTERFACE","certenroll/XCN_BCRYPT_SIGNATURE_INTERFACE","certenroll/XCN_BCRYPT_UNKNOWN_INTERFACE","security.algorithmtype_enum"]
old-location: security\algorithmtype_enum.htm
tech.root: security
ms.assetid: 1a3da2df-b3e2-45fa-bae7-a9c0bac8b210
ms.date: 12/05/2018
ms.keywords: AlgorithmType, AlgorithmType enumeration [Security], XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE, XCN_BCRYPT_CIPHER_INTERFACE, XCN_BCRYPT_HASH_INTERFACE, XCN_BCRYPT_RNG_INTERFACE, XCN_BCRYPT_SECRET_AGREEMENT_INTERFACE, XCN_BCRYPT_SIGNATURE_INTERFACE, XCN_BCRYPT_UNKNOWN_INTERFACE, certenroll/AlgorithmType, certenroll/XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE, certenroll/XCN_BCRYPT_CIPHER_INTERFACE, certenroll/XCN_BCRYPT_HASH_INTERFACE, certenroll/XCN_BCRYPT_RNG_INTERFACE, certenroll/XCN_BCRYPT_SECRET_AGREEMENT_INTERFACE, certenroll/XCN_BCRYPT_SIGNATURE_INTERFACE, certenroll/XCN_BCRYPT_UNKNOWN_INTERFACE, security.algorithmtype_enum
f1_keywords:
- certenroll/AlgorithmType
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- CertEnroll.h
api_name:
- AlgorithmType
targetos: Windows
req.typenames: AlgorithmType
req.redist: 
ms.custom: 19H1
---

# AlgorithmType enumeration


## -description


The <b>AlgorithmType</b> enumeration type specifies the intended purpose of a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic algorithm</a> supported by a cryptographic provider. Algorithms are typically classified by use into the following general categories:<ul>
<li>Signing</li>
<li>Hashing</li>
<li>Asymmetric encryption</li>
<li>Symmetric encryption</li>
<li>Key exchange</li>
</ul> This enumeration is used in the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a> interface.


## -enum-fields




### -field XCN_BCRYPT_UNKNOWN_INTERFACE

The algorithm type is not defined.


### -field XCN_BCRYPT_CIPHER_INTERFACE

The algorithm is used for symmetric encryption. This includes the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">RC2</a>, <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">RC4</a>, <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Data Encryption Standard</a> (DES), 3DED, and <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">AES</a> algorithms.


### -field XCN_BCRYPT_HASH_INTERFACE

The algorithm is used for hashing. This includes the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/m-gly">MD2</a>, <a href="https://docs.microsoft.com/windows/desktop/SecGloss/m-gly">MD4</a>, SHA1, SHA256, SHA384, SHA512 MAC, and <a href="https://docs.microsoft.com/windows/desktop/SecGloss/h-gly">Hash-Based Message Authentication Code</a> (HMAC) hash algorithms.


### -field XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE

The algorithm is used for <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">public key</a> encryption. This includes RSA.


### -field XCN_BCRYPT_SIGNATURE_INTERFACE

The algorithm is used for signing. This includes the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">RSA</a> algorithm, <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Digital Signature Algorithm</a> (DSA), and ECDSA algorithm.


### -field XCN_BCRYPT_SECRET_AGREEMENT_INTERFACE

The algorithm is used for key exchange. This includes the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Diffie-Hellman algorithm</a> and ECDH algorithm.


### -field XCN_BCRYPT_RNG_INTERFACE

The algorithm is used to generate a random number.


### -field XCN_BCRYPT_KEY_DERIVATION_INTERFACE




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-algorithmoperationflags">AlgorithmOperationFlags</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>
 

 

