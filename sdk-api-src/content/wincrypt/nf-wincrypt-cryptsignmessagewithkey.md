---
UID: NF:wincrypt.CryptSignMessageWithKey
title: CryptSignMessageWithKey function (wincrypt.h)
description: Signs a message by using a CSP's private key specified in the parameters.
helpviewer_keywords: ["CryptSignMessageWithKey","CryptSignMessageWithKey function [Security]","security.cryptsignmessagewithkey","wincrypt/CryptSignMessageWithKey"]
old-location: security\cryptsignmessagewithkey.htm
tech.root: security
ms.assetid: d31024bf-7022-440b-8134-a02578510357
ms.date: 12/05/2018
ms.keywords: CryptSignMessageWithKey, CryptSignMessageWithKey function [Security], security.cryptsignmessagewithkey, wincrypt/CryptSignMessageWithKey
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptSignMessageWithKey
 - wincrypt/CryptSignMessageWithKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptSignMessageWithKey
---

# CryptSignMessageWithKey function


## -description

The <b>CryptSignMessageWithKey</b> function signs a message by using a CSP's private key specified in the
parameters. A placeholder <b>SignerId</b> is created and stored in the message.

## -parameters

### -param pSignPara [in]

A pointer to 
a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_sign_message_para">CRYPT_KEY_SIGN_MESSAGE_PARA</a> structure that contains the signature parameters.

### -param pbToBeSigned [in]

A pointer to a buffer array that contains the message to be signed.

### -param cbToBeSigned [in]

The number of array elements in the <i>pbToBeSigned</i> buffer array.

### -param pbSignedBlob [out]

A pointer to a buffer to receive the encoded signed message. 




This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbSignedBlob [in, out]

A pointer to a <b>DWORD</b> value that indicates the size, in bytes, of the <i>pbSignedBlob</i> buffer. When the function returns, this variable contains the size, in bytes, of the signed and encoded message. 




<div class="alert"><b>Note</b>  When processing the data returned, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE).

For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 

The following lists the error codes most commonly returned by the 
		       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

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
The <a href="/windows/desktop/SecGloss/m-gly">message encoding type</a> is not valid. Currently only PKCS_7_ASN_ENCODING is supported. The <b>cbSize</b> in *<i>pSignPara</i> is not valid.

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