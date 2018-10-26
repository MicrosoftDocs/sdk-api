---
UID: NF:wincrypt.CryptHashCertificate
title: CryptHashCertificate function
author: windows-sdk-content
description: The CryptHashCertificate function hashes the entire encoded content of a certificate including its signature.
old-location: security\crypthashcertificate.htm
tech.root: seccrypto
ms.assetid: a5beba30-f32b-4d57-8a54-7d9096459c50
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CryptHashCertificate, CryptHashCertificate function [Security], _crypto2_crypthashcertificate, security.crypthashcertificate, wincrypt/CryptHashCertificate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptHashCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptHashCertificate function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptHashCertificate</b> function <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hashes</a> the entire encoded content of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a> including its signature.


## -parameters




### -param hCryptProv [in]

This parameter is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>A handle of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) to use to compute the hash. 


This parameter's data type is <b>HCRYPTPROV</b>.

Unless there is a strong reason for passing in a specific CSP in <i>hCryptProv</i>, zero is passed in. Passing in zero causes the default <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">RSA</a> or <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Digital Signature Standard</a> (DSS) provider to be acquired before doing hash, signature verification, or recipient encryption operations.




### -param Algid [in]

An 
						<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a> structure that specifies the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash algorithm</a> to use. If <i>Algid</i> is zero, the default hash algorithm, SHA1, is used.


### -param dwFlags [in]

Value to be passed to the hash API. For details, see 
<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a>.


### -param pbEncoded [in]

Address of the encoded content to be hashed.


### -param cbEncoded [in]

The size, in bytes, of the encoded content.


### -param pbComputedHash [out]

A pointer to a buffer to receive the computed hash. 




To set the size of this information for memory allocation purposes, this parameter can be <b>NULL</b>. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbComputedHash [in, out]

A pointer to a <b>DWORD</b> that contains the size, in bytes, of the buffer pointed to by the <i>pbComputedHash</i> parameter. When the function returns, the <b>DWORD</b> contains the number of bytes stored in the buffer. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications need to use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer. On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a>, 
<a href="https://msdn.microsoft.com/ed008c07-1a40-4075-bdaa-eb7f7e12d9c3">CryptGetHashParam</a> and 
<a href="https://msdn.microsoft.com/ec1482a2-c2cb-4c5f-af9c-d493134413d6">CryptHashData</a> might be propagated to this function.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b0c419b7-ebb3-42c6-9f6a-59b55a2db1b2">CryptHashPublicKeyInfo</a>



<a href="https://msdn.microsoft.com/84477054-dd76-4dde-b465-9edeaf192714">CryptHashToBeSigned</a>



<a href="cryptography_functions.htm">Data Management Functions</a>
 

 

