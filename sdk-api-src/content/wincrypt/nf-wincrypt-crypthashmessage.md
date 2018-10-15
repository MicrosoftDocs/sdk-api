---
UID: NF:wincrypt.CryptHashMessage
title: CryptHashMessage function
author: windows-sdk-content
description: Creates a hash of the message.
old-location: security\crypthashmessage.htm
tech.root: seccrypto
ms.assetid: 85a04c01-fd7c-4d87-b6e1-a0f2aea45d16
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CryptHashMessage, CryptHashMessage function [Security], _crypto2_crypthashmessage, security.crypthashmessage, wincrypt/CryptHashMessage
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
 - CryptHashMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptHashMessage function


## -description


The <b>CryptHashMessage</b> function creates a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of the message.


## -parameters




### -param pHashPara [in]

A pointer to a 
<a href="https://msdn.microsoft.com/60415136-3ac0-4fab-bdbf-faa16e8e43e1">CRYPT_HASH_MESSAGE_PARA</a> structure that contains the hash parameters.


### -param fDetachedHash [in]

If this parameter is set to <b>TRUE</b>, only <i>pbComputedHash</i> is encoded in <i>pbHashedBlob</i>. Otherwise, both <i>rgpbToBeHashed</i> and <i>pbComputedHash</i> are encoded.


### -param cToBeHashed [in]

The number of array elements in <i>rgpbToBeHashed</i> and <i>rgcbToBeHashed</i>. This parameter can only be one unless <i>fDetachedHash</i> is set to <b>TRUE</b>.


### -param rgpbToBeHashed [in]

An array of pointers to buffers that contain the contents to be hashed.


### -param rgcbToBeHashed [in]

An array of sizes, in bytes, of the buffers pointed to by <i>rgpbToBeHashed</i>.


### -param pbHashedBlob [out]

A pointer to a buffer to receive the hashed message encoded for transmission. 




This parameter can be <b>NULL</b> if the hashed message is not needed for additional processing or to set the size of the hashed message for memory allocation purposes. A hashed message will not be returned if this parameter is <b>NULL</b>. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbHashedBlob [in, out]

A pointer to a <b>DWORD</b> that specifies the size, in bytes, of the buffer pointed to by the <i>pbHashedBlob</i> parameter. When the function returns, this variable contains the size, in bytes, of the decrypted message copied to <i>pbHashedBlob</i>. This parameter must be the address of a <b>DWORD</b> and not <b>NULL</b> or the length of the buffer will not be returned. 




<div class="alert"><b>Note</b>  When processing the data returned, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer. On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

### -param pbComputedHash [out, optional]

A pointer to a buffer to receive the newly created hash value. This parameter can be <b>NULL</b> if the newly created hash is not needed for additional processing, or to set the size of the hash for memory allocation purposes. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbComputedHash [in, out, optional]

A pointer to a <b>DWORD</b> that specifies the size, in bytes, of the buffer pointed to by the <i>pbComputedHash</i> parameter. When the function returns, this <b>DWORD</b> contains the size, in bytes, of the newly created hash that was copied to <i>pbComputedHash</i>. 




<div class="alert"><b>Note</b>  When processing the data returned, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer. On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a>, 
<a href="https://msdn.microsoft.com/ec1482a2-c2cb-4c5f-af9c-d493134413d6">CryptHashData</a>, and 
<a href="https://msdn.microsoft.com/ed008c07-1a40-4075-bdaa-eb7f7e12d9c3">CryptGetHashParam</a> might be propagated to this function.</div>
<div> </div>
The <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns the following error codes most often.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
If the buffer specified by the <i>pbHashedBlob</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, into the variable pointed to by <i>pbHashedBlob</i>.

</td>
</tr>
</table>
 

If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/b529b9e2-9798-4548-a44f-c330524a3e6b">CryptVerifyDetachedMessageHash</a>



<a href="https://msdn.microsoft.com/3b5185b9-e24b-4302-a60c-74ccbd19077c">CryptVerifyMessageHash</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Simplified Message Functions</a>
 

 

