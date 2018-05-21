---
UID: NE:certenroll.AlgorithmOperationFlags
title: AlgorithmOperationFlags
author: windows-driver-content
description: Specifies the operations that an algorithm can perform.
old-location: security\algorithmoperationflags_enum.htm
old-project: SecCertEnroll
ms.assetid: 5fa7ee1e-f5ab-44c9-8ae4-a2940f0c6289
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: AlgorithmOperationFlags, AlgorithmOperationFlags enumeration [Security], XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION, XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION, XCN_NCRYPT_CIPHER_OPERATION, XCN_NCRYPT_EXACT_MATCH_OPERATION, XCN_NCRYPT_HASH_OPERATION, XCN_NCRYPT_NO_OPERATION, XCN_NCRYPT_PREFERENCE_MASK_OPERATION, XCN_NCRYPT_PREFER_NON_SIGNATURE_OPERATION, XCN_NCRYPT_PREFER_SIGNATURE_ONLY_OPERATION, XCN_NCRYPT_RNG_OPERATION, XCN_NCRYPT_SECRET_AGREEMENT_OPERATION, XCN_NCRYPT_SIGNATURE_OPERATION, certenroll/AlgorithmOperationFlags, certenroll/XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION, certenroll/XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION, certenroll/XCN_NCRYPT_CIPHER_OPERATION, certenroll/XCN_NCRYPT_EXACT_MATCH_OPERATION, certenroll/XCN_NCRYPT_HASH_OPERATION, certenroll/XCN_NCRYPT_NO_OPERATION, certenroll/XCN_NCRYPT_PREFERENCE_MASK_OPERATION, certenroll/XCN_NCRYPT_PREFER_NON_SIGNATURE_OPERATION, certenroll/XCN_NCRYPT_PREFER_SIGNATURE_ONLY_OPERATION, certenroll/XCN_NCRYPT_RNG_OPERATION, certenroll/XCN_NCRYPT_SECRET_AGREEMENT_OPERATION, certenroll/XCN_NCRYPT_SIGNATURE_OPERATION, security.algorithmoperationflags_enum
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
req.typenames: AlgorithmOperationFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	CertEnroll.h
api_name:
-	AlgorithmOperationFlags
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# AlgorithmOperationFlags enumeration


## -description


The <b>AlgorithmOperationFlags</b> enumeration type specifies the operations that an algorithm can perform. This enumeration is used in the following interfaces to retrieve the operational capabilities of a cryptographic provider or status information based on those capabilities.<ul>
<li>
<a href="https://msdn.microsoft.com/08eba616-2e96-40cd-9fda-8549de98c138">ICspAlgorithm</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a>
</li>
<li>
<a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a>
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

The algorithm can be  used for <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">symmetric encryption</a>. This includes the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">RC2</a>, <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">RC4</a>, <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Data Encryption Standard</a> (DES), 3DED, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff544012">AES</a> algorithms.


### -field XCN_NCRYPT_HASH_OPERATION

The algorithm can be used for hashing. This includes the <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">MD2</a>, <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">MD4</a>, SHA1, SHA256, SHA384, SHA512 MAC, and <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">Hash-Based Message Authentication Code</a> (HMAC) <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hashing algorithms</a>.


### -field XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION

The algorithm can be used for <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> encryption. This includes <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">RSA</a>.


### -field XCN_NCRYPT_SECRET_AGREEMENT_OPERATION

The algorithm can used for key exchange. This includes the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Diffie-Hellman algorithm</a> and ECDH algorithm.


### -field XCN_NCRYPT_SIGNATURE_OPERATION

The algorithm can be  used for signing. This includes the RSA algorithm, <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Digital Signature Algorithm</a> (DSA), and ECDSA algorithm.


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

Signature algorithms are preferred but not required. An encryption algorithm may be chosen instead. This is used when searching for <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) status information based on supported operational capability.


### -field XCN_NCRYPT_PREFER_NON_SIGNATURE_OPERATION

An encryption algorithm (such as that identified by the <b>XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION</b> or <b>XCN_NCRYPT_SECRET_AGREEMENT_OPERATION</b> flags) is preferred but not required. A signature algorithm may be chosen instead. This is used when searching for CSP status information based on supported operational capability.


### -field XCN_NCRYPT_EXACT_MATCH_OPERATION

Only an algorithm that exactly matches the specified operations is selected.


### -field XCN_NCRYPT_PREFERENCE_MASK_OPERATION

Use to mask the algorithm operation preference.


## -see-also




<a href="https://msdn.microsoft.com/1a3da2df-b3e2-45fa-bae7-a9c0bac8b210">AlgorithmType</a>



<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>
 

 

