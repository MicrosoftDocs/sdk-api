---
UID: NF:wincrypt.CryptVerifyMessageHash
title: CryptVerifyMessageHash function
author: windows-sdk-content
description: The CryptVerifyMessageHash function verifies the hash of specified content.
old-location: security\cryptverifymessagehash.htm
old-project: SecCrypto
ms.assetid: 3b5185b9-e24b-4302-a60c-74ccbd19077c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CryptVerifyMessageHash, CryptVerifyMessageHash function [Security], _crypto2_cryptverifymessagehash, security.cryptverifymessagehash, wincrypt/CryptVerifyMessageHash
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptVerifyMessageHash
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptVerifyMessageHash function


## -description


The <b>CryptVerifyMessageHash</b> function verifies the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of specified content.


## -parameters




### -param pHashPara [in]

A pointer to a 
<a href="https://msdn.microsoft.com/60415136-3ac0-4fab-bdbf-faa16e8e43e1">CRYPT_HASH_MESSAGE_PARA</a> structure containing hash parameters.


### -param pbHashedBlob [in]

A pointer to a buffer containing original content and its hash.


### -param cbHashedBlob [in]

The size, in bytes, of the original hash buffer.


### -param pbToBeHashed [out]

A pointer to a buffer to receive the original content that was hashed. 




This parameter can be <b>NULL</b> if the original content is not needed for additional processing, or to set the size of the original content for memory allocation purposes. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbToBeHashed [in, out]

A pointer to a <b>DWORD</b> specifying the size, in bytes, of the <i>pbToBeHashed</i> buffer. When the function returns, this variable contains the size, in bytes, of the original content copied to <i>pbToBeHashed</i>. The original content will not be returned if this parameter is <b>NULL</b>. 




<div class="alert"><b>Note</b>  When processing the data returned, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

### -param pbComputedHash [out, optional]

A pointer to a buffer to receive the computed hash. This parameter can be <b>NULL</b> if the created hash is not needed for additional processing, or to set the size of the original content for memory allocation purposes. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbComputedHash [in, out, optional]

A pointer to a <b>DWORD</b> specifying the size, in bytes, of the <i>pbComputedHash</i> buffer. When the function returns, this variable contains the size, in bytes, of the created hash. The hash is not returned if this parameter is <b>NULL</b>. 




<div class="alert"><b>Note</b>  When processing the data returned, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns



If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE).

For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following lists the error codes most commonly returned by the 
		       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNEXPECTED_MSG_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Not a hashed cryptographic message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding type</a> is not valid. Currently only PKCS_7_ASN_ENCODING is supported. The <b>cbSize</b> in *<i>pHashPara</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pbToBeHashed</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code, and stores the required buffer size, in bytes, into the variable pointed to by <i>pcbToBeHashed</i>.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a>, 
<a href="https://msdn.microsoft.com/ec1482a2-c2cb-4c5f-af9c-d493134413d6">CryptHashData</a>, and 
<a href="https://msdn.microsoft.com/ed008c07-1a40-4075-bdaa-eb7f7e12d9c3">CryptGetHashParam</a> might be propagated to this function. <p class="note">If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>. 

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b529b9e2-9798-4548-a44f-c330524a3e6b">CryptVerifyDetachedMessageHash</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Simplified Message Functions</a>
 

 

