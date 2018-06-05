---
UID: NE:certenroll.AlgorithmType
title: AlgorithmType
author: windows-sdk-content
description: Specifies the intended purpose of a cryptographic algorithm supported by a cryptographic provider.
old-location: security\algorithmtype_enum.htm
old-project: SecCertEnroll
ms.assetid: 1a3da2df-b3e2-45fa-bae7-a9c0bac8b210
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: AlgorithmType, AlgorithmType enumeration [Security], XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE, XCN_BCRYPT_CIPHER_INTERFACE, XCN_BCRYPT_HASH_INTERFACE, XCN_BCRYPT_RNG_INTERFACE, XCN_BCRYPT_SECRET_AGREEMENT_INTERFACE, XCN_BCRYPT_SIGNATURE_INTERFACE, XCN_BCRYPT_UNKNOWN_INTERFACE, certenroll/AlgorithmType, certenroll/XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE, certenroll/XCN_BCRYPT_CIPHER_INTERFACE, certenroll/XCN_BCRYPT_HASH_INTERFACE, certenroll/XCN_BCRYPT_RNG_INTERFACE, certenroll/XCN_BCRYPT_SECRET_AGREEMENT_INTERFACE, certenroll/XCN_BCRYPT_SIGNATURE_INTERFACE, certenroll/XCN_BCRYPT_UNKNOWN_INTERFACE, security.algorithmtype_enum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: AlgorithmType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	CertEnroll.h
api_name:
-	AlgorithmType
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# AlgorithmType enumeration


## -description


The <b>AlgorithmType</b> enumeration type specifies the intended purpose of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic algorithm</a> supported by a cryptographic provider. Algorithms are typically classified by use into the following general categories:<ul>
<li>Signing</li>
<li>Hashing</li>
<li>Asymmetric encryption</li>
<li>Symmetric encryption</li>
<li>Key exchange</li>
</ul> This enumeration is used in the <a href="https://msdn.microsoft.com/08eba616-2e96-40cd-9fda-8549de98c138">ICspAlgorithm</a> interface.


## -enum-fields




### -field XCN_BCRYPT_UNKNOWN_INTERFACE

The algorithm type is not defined.


### -field XCN_BCRYPT_CIPHER_INTERFACE

The algorithm is used for symmetric encryption. This includes the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">RC2</a>, <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">RC4</a>, <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Data Encryption Standard</a> (DES), 3DED, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff544012">AES</a> algorithms.


### -field XCN_BCRYPT_HASH_INTERFACE

The algorithm is used for hashing. This includes the <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">MD2</a>, <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">MD4</a>, SHA1, SHA256, SHA384, SHA512 MAC, and <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">Hash-Based Message Authentication Code</a> (HMAC) hash algorithms.


### -field XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE

The algorithm is used for <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> encryption. This includes RSA.


### -field XCN_BCRYPT_SIGNATURE_INTERFACE

The algorithm is used for signing. This includes the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">RSA</a> algorithm, <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Digital Signature Algorithm</a> (DSA), and ECDSA algorithm.


### -field XCN_BCRYPT_SECRET_AGREEMENT_INTERFACE

The algorithm is used for key exchange. This includes the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Diffie-Hellman algorithm</a> and ECDH algorithm.


### -field XCN_BCRYPT_RNG_INTERFACE

The algorithm is used to generate a random number.


### -field XCN_BCRYPT_KEY_DERIVATION_INTERFACE




## -see-also




<a href="https://msdn.microsoft.com/5fa7ee1e-f5ab-44c9-8ae4-a2940f0c6289">AlgorithmOperationFlags</a>



<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>
 

 

