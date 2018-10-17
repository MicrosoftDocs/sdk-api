---
UID: NF:wincrypt.CryptSignMessageWithKey
title: CryptSignMessageWithKey function
author: windows-sdk-content
description: Signs a message by using a CSP's private key specified in the parameters.
old-location: security\cryptsignmessagewithkey.htm
tech.root: seccrypto
ms.assetid: d31024bf-7022-440b-8134-a02578510357
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: CryptSignMessageWithKey, CryptSignMessageWithKey function [Security], security.cryptsignmessagewithkey, wincrypt/CryptSignMessageWithKey
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
 - CryptSignMessageWithKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptSignMessageWithKey function


## -description


The <b>CryptSignMessageWithKey</b> function signs a message by using a CSP's private key specified in the
parameters. A placeholder <b>SignerId</b> is created and stored in the message.


## -parameters




### -param pSignPara [in]

A pointer to 
a <a href="https://msdn.microsoft.com/d5426ad6-2181-42ce-99f2-cc6cc83e20a8">CRYPT_KEY_SIGN_MESSAGE_PARA</a> structure that contains the signature parameters.


### -param pbToBeSigned [in]

A pointer to a buffer array that contains the message to be signed.


### -param cbToBeSigned [in]

The number of array elements in the <i>pbToBeSigned</i> buffer array.


### -param pbSignedBlob [out]

A pointer to a buffer to receive the encoded signed message. 




This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbSignedBlob [in, out]

A pointer to a <b>DWORD</b> value that indicates the size, in bytes, of the <i>pbSignedBlob</i> buffer. When the function returns, this variable contains the size, in bytes, of the signed and encoded message. 




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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pbSignedBlob</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, into the variable pointed to by <i>pcbSignedBlob</i>.

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
 



