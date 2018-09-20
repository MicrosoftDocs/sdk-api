---
UID: NC:wincrypt.PFN_CRYPT_EXTRACT_ENCODED_SIGNATURE_PARAMETERS_FUNC
title: PFN_CRYPT_EXTRACT_ENCODED_SIGNATURE_PARAMETERS_FUNC
author: windows-sdk-content
description: Called to decode and return the hash algorithm identifier and optionally the signature parameters.
old-location: security\pfn_crypt_extract_encoded_signature_parameters_func.htm
tech.root: seccrypto
ms.assetid: 2b990a1d-8913-49bc-920f-253b38871eb6
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: PFN_CRYPT_EXTRACT_ENCODED_SIGNATURE_PARAMETERS_FUNC, PFN_CRYPT_EXTRACT_ENCODED_SIGNATURE_PARAMETERS_FUNC callback, PFN_CRYPT_EXTRACT_ENCODED_SIGNATURE_PARAMETERS_FUNC callback function [Security], security.pfn_crypt_extract_encoded_signature_parameters_func, wincrypt/PFN_CRYPT_EXTRACT_ENCODED_SIGNATURE_PARAMETERS_FUNC
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
 - PFN_CRYPT_EXTRACT_ENCODED_SIGNATURE_PARAMETERS_FUNC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CRYPT_EXTRACT_ENCODED_SIGNATURE_PARAMETERS_FUNC callback function


## -description


If a signature contains encoded parameters, the <b>PFN_CRYPT_EXTRACT_ENCODED_SIGNATURE_PARAMETERS_FUNC</b> callback function is called to decode and return the hash algorithm identifier and optionally the signature parameters.


## -parameters




### -param dwCertEncodingType [in]

Specifies the type of encoding used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>



### -param pSignatureAlgorithm [in]

A pointer to a <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the signature <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and its optional encoded parameters.


#### - **ppvDecodedSignPara [out, optional]

A pointer to an address for the decoded and allocated signature parameters data structure. Returning the decoded buffer is optional.


### -param *ppwszCNGHashAlgid [out]

A pointer to an address for the allocated Unicode string that represents the CNG hash algorithm identifier extracted from the encoded signature parameters. If this function returns <b>TRUE</b>, a non-<b>NULL</b> pointer must be returned.


#### - ppvDecodedSignPara [out, optional]

A pointer to an address for the decoded and allocated signature parameters data structure. Returning the decoded buffer is optional.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If this callback function does not support the signature algorithm, it must return <b>FALSE</b> and call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> with <b>ERROR_NOT_SUPPORTED</b>.




## -remarks



Memory for the <i>ppvDecodedSignPara</i> and <i>ppwszCNGHashAlgid</i> parameters must be allocated by using the <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> function.

You can use <a href="cryptography_functions.htm">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constant for this purpose.

<table>
<tr>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td>CRYPT_OID_EXTRACT_ENCODED_SIGNATURE_PARAMETERS_FUNC</td>
<td>"CryptDllExtractEncodedSignatureParameters"</td>
</tr>
</table>
 



