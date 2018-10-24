---
UID: NC:wincrypt.PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC
title: PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC
author: windows-sdk-content
description: Called by CryptExportPublicKeyInfoEx to export a public key BLOB and encode it.
old-location: security\pfn_crypt_export_public_key_info_ex2_func.htm
tech.root: SecCrypto
ms.assetid: 37315539-64f8-4708-8a17-f80a2869e6b3
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC, PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC callback, PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC callback function [Security], security.pfn_crypt_export_public_key_info_ex2_func, wincrypt/PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC
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
 - PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC callback function


## -description


The <b>PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC</b> callback function is called by <a href="https://msdn.microsoft.com/38274222-90b3-4038-86d3-6b2813100ce2">CryptExportPublicKeyInfoEx</a> to export a public key BLOB and encode it.


## -parameters




### -param hNCryptKey [in]

A handle of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) to use when exporting the public key information. This handle must be an <b>NCRYPT_KEY_HANDLE</b> handle that has been created by using the <a href="https://msdn.microsoft.com/581c5d89-730d-4d8c-b3bb-a28edec25910">NCryptOpenKey</a> function.


### -param dwCertEncodingType [in]

A value that specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pszPublicKeyObjId [in]

A pointer to a string that contains the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key algorithm</a>.


### -param dwFlags [in]

A value that indicates how the public key information  is exported. This can be zero.


### -param *pvAuxInfo [in, optional]

This parameter is reserved for future use and  must be set to <b>NULL</b>.


### -param pInfo [out, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a>  structure to receive the public key information to be exported.

This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param *pcbInfo [in, out]

A pointer to a <b>DWORD</b> that contains the size, in bytes, of the buffer pointed to by the <i>pInfo</i> parameter. When the function returns, the <b>DWORD</b> contains the number of bytes stored in the buffer.

<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications need to use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If this callback function does not support the signature algorithm, it must return <b>FALSE</b> and call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> with <b>ERROR_NOT_SUPPORTED</b>.




## -remarks



You can use <a href="cryptography_functions.htm">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constant for this purpose.

<table>
<tr>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td>CRYPT_OID_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC</td>
<td>"CryptDllExportPublicKeyInfoEx2"</td>
</tr>
</table>
 



