---
UID: NE:certenroll.AlgorithmType
title: AlgorithmType
author: windows-sdk-content
description: Specifies the intended purpose of a cryptographic algorithm supported by a cryptographic provider.
old-location: security\algorithmtype_enum.htm
tech.root: SecCertEnroll
ms.assetid: 1a3da2df-b3e2-45fa-bae7-a9c0bac8b210
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AlgorithmType, AlgorithmType enumeration [Security], XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE, XCN_BCRYPT_CIPHER_INTERFACE, XCN_BCRYPT_HASH_INTERFACE, XCN_BCRYPT_RNG_INTERFACE, XCN_BCRYPT_SECRET_AGREEMENT_INTERFACE, XCN_BCRYPT_SIGNATURE_INTERFACE, XCN_BCRYPT_UNKNOWN_INTERFACE, certenroll/AlgorithmType, certenroll/XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE, certenroll/XCN_BCRYPT_CIPHER_INTERFACE, certenroll/XCN_BCRYPT_HASH_INTERFACE, certenroll/XCN_BCRYPT_RNG_INTERFACE, certenroll/XCN_BCRYPT_SECRET_AGREEMENT_INTERFACE, certenroll/XCN_BCRYPT_SIGNATURE_INTERFACE, certenroll/XCN_BCRYPT_UNKNOWN_INTERFACE, security.algorithmtype_enum
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: AlgorithmType
req.redist: 
---

# AlgorithmType enumeration


## -description


The <b>AlgorithmType</b> enumeration type specifies the intended purpose of a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">cryptographic algorithm</a> supported by a cryptographic provider. Algorithms are typically classified by use into the following general categories:<ul>
<li>Signing</li>
<li>Hashing</li>
<li>Asymmetric encryption</li>
<li>Symmetric encryption</li>
<li>Key exchange</li>
</ul> This enumeration is used in the <a href="https://msdn.microsoft.com/en-us/library/Aa375947(v=VS.85).aspx">ICspAlgorithm</a> interface.


## -enum-fields




### -field XCN_BCRYPT_UNKNOWN_INTERFACE

The algorithm type is not defined.


### -field XCN_BCRYPT_CIPHER_INTERFACE

The algorithm is used for symmetric encryption. This includes the <a href="https://msdn.microsoft.com/en-us/library/ms721604(v=VS.85).aspx">RC2</a>, <a href="https://msdn.microsoft.com/en-us/library/ms721604(v=VS.85).aspx">RC4</a>, <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Data Encryption Standard</a> (DES), 3DED, and <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">AES</a> algorithms.


### -field XCN_BCRYPT_HASH_INTERFACE

The algorithm is used for hashing. This includes the <a href="https://msdn.microsoft.com/en-us/library/ms721594(v=VS.85).aspx">MD2</a>, <a href="https://msdn.microsoft.com/en-us/library/ms721594(v=VS.85).aspx">MD4</a>, SHA1, SHA256, SHA384, SHA512 MAC, and <a href="https://msdn.microsoft.com/en-us/library/ms721586(v=VS.85).aspx">Hash-Based Message Authentication Code</a> (HMAC) hash algorithms.


### -field XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE

The algorithm is used for <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">public key</a> encryption. This includes RSA.


### -field XCN_BCRYPT_SIGNATURE_INTERFACE

The algorithm is used for signing. This includes the <a href="https://msdn.microsoft.com/en-us/library/ms721604(v=VS.85).aspx">RSA</a> algorithm, <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Digital Signature Algorithm</a> (DSA), and ECDSA algorithm.


### -field XCN_BCRYPT_SECRET_AGREEMENT_INTERFACE

The algorithm is used for key exchange. This includes the <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Diffie-Hellman algorithm</a> and ECDH algorithm.


### -field XCN_BCRYPT_RNG_INTERFACE

The algorithm is used to generate a random number.


### -field XCN_BCRYPT_KEY_DERIVATION_INTERFACE




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374821(v=VS.85).aspx">AlgorithmOperationFlags</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374846(v=VS.85).aspx">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>
 

 

