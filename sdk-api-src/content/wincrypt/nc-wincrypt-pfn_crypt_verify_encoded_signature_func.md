---
UID: NC:wincrypt.PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC
title: PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC
author: windows-sdk-content
description: Called to decrypt an encoded signature and compare it to a computed hash.
old-location: security\pfn_crypt_verify_encoded_signature_func.htm
tech.root: seccrypto
ms.assetid: 0093ce11-8b72-403d-a3fd-3eaf2dc29d71
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC, PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC callback, PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC callback function [Security], security.pfn_crypt_verify_encoded_signature_func, wincrypt/PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: wincrypt.h
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
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC callback function


## -description


The <b>PFN_CRYPT_VERIFY_ENCODED_SIGNATURE_FUNC</b> callback function is called to decrypt an encoded signature and compare it to a computed hash.


## -parameters




### -param dwCertEncodingType [in]

Specifies the type of encoding used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>



### -param pPubKeyInfo [in]

The address of a <a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure that contains the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> to use to verify the signature. You can use this with <a href="https://msdn.microsoft.com/c73f2499-75e9-4146-ae4c-0e949206ea37">CryptImportPublicKeyInfoEx2</a> to get a <b>BCRYPT_KEY_HANDLE</b>.


### -param pSignatureAlgorithm [in]

A pointer to a <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the signature <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and its optional encoded parameters.


### -param *pvDecodedSignPara [in, optional]

An optional pointer to the decoded signature parameters data structure previously returned by the <a href="https://msdn.microsoft.com/2b990a1d-8913-49bc-920f-253b38871eb6">PFN_CRYPT_EXTRACT_ENCODED_SIGNATURE_PARAMETERS_FUNC</a>  function.


### -param pwszCNGPubKeyAlgid [in]

A Unicode string that contains the Cryptography API: Next Generation (CNG) <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key algorithm</a> identifier that corresponds to <i>pSignatureAlgorithm</i>-&gt;<b>pszObjId</b>.


### -param pwszCNGHashAlgid [in]

A Unicode string that contains the CNG <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hashing algorithm</a> identifier that corresponds to <i>pSignatureAlgorithm</i>-&gt;<b>pszObjId</b> or to a hash algorithm identifier in <i>pvDecodedSignPara</i>.


### -param *pbComputedHash [in]

A pointer to the computed hash bytes returned by the <a href="https://msdn.microsoft.com/82a7c3d9-c01b-46d0-8b54-694dc0d8ffdd">BCryptFinishHash</a> function that corresponds to <i>pwszCNGHashAlgid</i>.


### -param cbComputedHash [in]

A value that represents the length, in bytes, of the computed hash.


### -param *pbSignature [in]

A pointer to the encoded signature bytes.


### -param cbSignature [in]

A value that represents the length, in bytes, of the encoded signature.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If this callback function does not support the signature algorithm, it must return <b>FALSE</b> and call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> with <b>ERROR_NOT_SUPPORTED</b>.




## -remarks



You can use <a href="cryptography_functions.htm">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constant for this purpose.

<table>
<tr>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td>CRYPT_OID_VERIFY_ENCODED_SIGNATURE_FUNC</td>
<td>"CryptDllVerifyEncodedSignature"</td>
</tr>
</table>
 



