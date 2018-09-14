---
UID: NE:certenroll.AlgorithmOperationFlags
title: AlgorithmOperationFlags
author: windows-sdk-content
description: Specifies the operations that an algorithm can perform.
old-location: security\algorithmoperationflags_enum.htm
tech.root: seccertenroll
ms.assetid: 5fa7ee1e-f5ab-44c9-8ae4-a2940f0c6289
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: AlgorithmOperationFlags, AlgorithmOperationFlags enumeration [Security], XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION, XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION, XCN_NCRYPT_CIPHER_OPERATION, XCN_NCRYPT_EXACT_MATCH_OPERATION, XCN_NCRYPT_HASH_OPERATION, XCN_NCRYPT_NO_OPERATION, XCN_NCRYPT_PREFERENCE_MASK_OPERATION, XCN_NCRYPT_PREFER_NON_SIGNATURE_OPERATION, XCN_NCRYPT_PREFER_SIGNATURE_ONLY_OPERATION, XCN_NCRYPT_RNG_OPERATION, XCN_NCRYPT_SECRET_AGREEMENT_OPERATION, XCN_NCRYPT_SIGNATURE_OPERATION, certenroll/AlgorithmOperationFlags, certenroll/XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION, certenroll/XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION, certenroll/XCN_NCRYPT_CIPHER_OPERATION, certenroll/XCN_NCRYPT_EXACT_MATCH_OPERATION, certenroll/XCN_NCRYPT_HASH_OPERATION, certenroll/XCN_NCRYPT_NO_OPERATION, certenroll/XCN_NCRYPT_PREFERENCE_MASK_OPERATION, certenroll/XCN_NCRYPT_PREFER_NON_SIGNATURE_OPERATION, certenroll/XCN_NCRYPT_PREFER_SIGNATURE_ONLY_OPERATION, certenroll/XCN_NCRYPT_RNG_OPERATION, certenroll/XCN_NCRYPT_SECRET_AGREEMENT_OPERATION, certenroll/XCN_NCRYPT_SIGNATURE_OPERATION, security.algorithmoperationflags_enum
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
 - AlgorithmOperationFlags
product: Windows
targetos: Windows
req.typenames: AlgorithmOperationFlags
req.redist: 
---

# AlgorithmOperationFlags enumeration


## -description


The <b>AlgorithmOperationFlags</b> enumeration type specifies the operations that an algorithm can perform. This enumeration is used in the following interfaces to retrieve the operational capabilities of a cryptographic provider or status information based on those capabilities.<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375947(v=VS.85).aspx">ICspAlgorithm</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375968(v=VS.85).aspx">ICspInformations</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376761(v=VS.85).aspx">ICspStatuses</a>
</li>
</ul>


The binary format of the flags are as follows.
<pre class="syntax" xml:space="preserve"><code>XCN_NCRYPT_NO_OPERATION                     = 00000000 00000000 00000000
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
</code></pre>

## -enum-fields




### -field XCN_NCRYPT_NO_OPERATION

No operation is specified.


### -field XCN_NCRYPT_CIPHER_OPERATION

The algorithm can be  used for <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">symmetric encryption</a>. This includes the <a href="https://msdn.microsoft.com/en-us/library/ms721604(v=VS.85).aspx">RC2</a>, <a href="https://msdn.microsoft.com/en-us/library/ms721604(v=VS.85).aspx">RC4</a>, <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Data Encryption Standard</a> (DES), 3DED, and <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">AES</a> algorithms.


### -field XCN_NCRYPT_HASH_OPERATION

The algorithm can be used for hashing. This includes the <a href="https://msdn.microsoft.com/en-us/library/ms721594(v=VS.85).aspx">MD2</a>, <a href="https://msdn.microsoft.com/en-us/library/ms721594(v=VS.85).aspx">MD4</a>, SHA1, SHA256, SHA384, SHA512 MAC, and <a href="https://msdn.microsoft.com/en-us/library/ms721586(v=VS.85).aspx">Hash-Based Message Authentication Code</a> (HMAC) <a href="https://msdn.microsoft.com/en-us/library/ms721586(v=VS.85).aspx">hashing algorithms</a>.


### -field XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION

The algorithm can be used for <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">public key</a> encryption. This includes <a href="https://msdn.microsoft.com/en-us/library/ms721604(v=VS.85).aspx">RSA</a>.


### -field XCN_NCRYPT_SECRET_AGREEMENT_OPERATION

The algorithm can used for key exchange. This includes the <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Diffie-Hellman algorithm</a> and ECDH algorithm.


### -field XCN_NCRYPT_SIGNATURE_OPERATION

The algorithm can be  used for signing. This includes the RSA algorithm, <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Digital Signature Algorithm</a> (DSA), and ECDSA algorithm.


### -field XCN_NCRYPT_RNG_OPERATION

The algorithm can be used to generate a random number.


### -field XCN_NCRYPT_KEY_DERIVATION_OPERATION


### -field XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION

The algorithm can be used for public key encryption, key exchange, and signing. This is a bitwise-<b>OR</b> combination of the following constants:

<ul>
<li>XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION</li>
<li>XCN_NCRYPT_SECRET_AGREEMENT_OPERATION</li>
<li>XCN_NCRYPT_SIGNATURE_OPERATION</li>
</ul>

### -field XCN_NCRYPT_PREFER_SIGNATURE_ONLY_OPERATION

Signature algorithms are preferred but not required. An encryption algorithm may be chosen instead. This is used when searching for <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">cryptographic service provider</a> (CSP) status information based on supported operational capability.


### -field XCN_NCRYPT_PREFER_NON_SIGNATURE_OPERATION

An encryption algorithm (such as that identified by the <b>XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION</b> or <b>XCN_NCRYPT_SECRET_AGREEMENT_OPERATION</b> flags) is preferred but not required. A signature algorithm may be chosen instead. This is used when searching for CSP status information based on supported operational capability.


### -field XCN_NCRYPT_EXACT_MATCH_OPERATION

Only an algorithm that exactly matches the specified operations is selected.


### -field XCN_NCRYPT_PREFERENCE_MASK_OPERATION

Use to mask the algorithm operation preference.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374827(v=VS.85).aspx">AlgorithmType</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374846(v=VS.85).aspx">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>
 

 

