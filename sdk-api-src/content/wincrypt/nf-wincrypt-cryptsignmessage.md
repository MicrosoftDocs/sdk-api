---
UID: NF:wincrypt.CryptSignMessage
title: CryptSignMessage function
author: windows-sdk-content
description: The CryptSignMessage function creates a hash of the specified content, signs the hash, and then encodes both the original message content and the signed hash.
old-location: security\cryptsignmessage.htm
old-project: seccrypto
ms.assetid: f14f7c7b-14ac-40a7-9a49-d1a899ecc52a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CryptSignMessage, CryptSignMessage function [Security], _crypto2_cryptsignmessage, security.cryptsignmessage, wincrypt/CryptSignMessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.redist: 
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
 - CryptSignMessage
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptSignMessage function


## -description


The <b>CryptSignMessage</b> function creates a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of the specified content, signs the hash, and then encodes both the original message content and the signed hash.


## -parameters




### -param pSignPara [in]

A pointer to 
<a href="https://msdn.microsoft.com/1601d860-6054-4650-a033-ea088655b7e4">CRYPT_SIGN_MESSAGE_PARA</a> structure containing the signature parameters.


### -param fDetachedSignature [in]

<b>TRUE</b> if this is to be a detached signature. Otherwise, <b>FALSE</b>. If this parameter is set to <b>TRUE</b>, only the signed hash is encoded in <i>pbSignedBlob</i>. Otherwise, both <i>rgpbToBeSigned</i> and the signed hash are encoded.


### -param cToBeSigned [in]

Count of the number of array elements in <i>rgpbToBeSigned</i> and <i>rgpbToBeSigned</i>. This parameter must be set to one unless <i>fDetachedSignature</i> is set to <b>TRUE</b>.


### -param rgpbToBeSigned [in]

Array of pointers to buffers that contain the contents to be signed.


### -param rgcbToBeSigned [in]

Array of sizes, in bytes, of the content buffers pointed to in <i>rgpbToBeSigned</i>.
					


### -param pbSignedBlob [out]

A pointer to a buffer to receive the encoded signed hash, if <i>fDetachedSignature</i> is <b>TRUE</b>, or to both the encoded content and signed hash if <i>fDetachedSignature</i> is <b>FALSE</b>. 




This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbSignedBlob [in, out]

A pointer to a <b>DWORD</b> specifying the size, in bytes, of the <i>pbSignedBlob</i> buffer. When the function returns, this variable contains the size, in bytes, of the signed and encoded message. 




<div class="alert"><b>Note</b>  When processing the data returned, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>).

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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pbSignedBlob</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code, and stores the required buffer size, in bytes, into the variable pointed to by <i>pcbSignedBlob</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding type</a> is not valid. Currently only PKCS_7_ASN_ENCODING is supported. The <b>cbSize</b> in *<i>pSignPara</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NO_KEY_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The <i>pSigningCert</i> in *<i>pSignPara</i> does not have a CERT_KEY_PROV_INFO_PROP_ID or CERT_KEY_CONTEXT_PROP_ID property.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a>, 
<a href="https://msdn.microsoft.com/ec1482a2-c2cb-4c5f-af9c-d493134413d6">CryptHashData</a>, and 
<a href="https://msdn.microsoft.com/9cf0de04-fdad-457d-8137-16d98f915cd5">CryptSignHash</a> might be propagated to this function.</div>
<div> </div>
If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/0ab234f2-a681-463f-8ba8-b23b05cf2626">CryptSignAndEncryptMessage</a>



<a href="https://msdn.microsoft.com/03411e7a-b097-4059-a198-3d412ae40e38">CryptVerifyMessageSignature</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Simplified Message Functions</a>
 

 

