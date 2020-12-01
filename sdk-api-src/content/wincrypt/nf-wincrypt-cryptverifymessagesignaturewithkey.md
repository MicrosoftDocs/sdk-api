---
UID: NF:wincrypt.CryptVerifyMessageSignatureWithKey
title: CryptVerifyMessageSignatureWithKey function (wincrypt.h)
description: Verifies a signed message's signature by using specified public key information.
helpviewer_keywords: ["CryptVerifyMessageSignatureWithKey","CryptVerifyMessageSignatureWithKey function [Security]","security.cryptverifymessagesignaturewithkey","wincrypt/CryptVerifyMessageSignatureWithKey"]
old-location: security\cryptverifymessagesignaturewithkey.htm
tech.root: security
ms.assetid: 6fe0f9ee-1838-4eb7-8254-05b878eb8f56
ms.date: 12/05/2018
ms.keywords: CryptVerifyMessageSignatureWithKey, CryptVerifyMessageSignatureWithKey function [Security], security.cryptverifymessagesignaturewithkey, wincrypt/CryptVerifyMessageSignatureWithKey
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
 - CryptVerifyMessageSignatureWithKey
 - wincrypt/CryptVerifyMessageSignatureWithKey
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
 - CryptVerifyMessageSignatureWithKey
---

# CryptVerifyMessageSignatureWithKey function


## -description

The <b>CryptVerifyMessageSignatureWithKey</b> function verifies a signed message's signature by using specified public key information.

## -parameters

### -param pVerifyPara [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_verify_message_para">CRYPT_KEY_VERIFY_MESSAGE_PARA</a> structure that contains verification parameters.

### -param pPublicKeyInfo [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure that contains the public key that is used to verify the signed
message. If <b>NULL</b>, the signature is not verified.

### -param pbSignedBlob [in]

A pointer to a buffer that contains the signed message.

### -param cbSignedBlob [in]

The size, in bytes, of the signed message buffer.

### -param pbDecoded [out]

A pointer to a buffer to receive the decoded message. 




This parameter can be <b>NULL</b> if the decoded message is not needed for additional processing or to set the size of the message for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbDecoded [in, out]

A pointer to a <b>DWORD</b> value that specifies the size, in bytes, of the <i>pbDecoded</i> buffer. When the function returns, this <b>DWORD</b> contains the size, in bytes, of the decoded message. The decoded message will not be returned if this parameter is <b>NULL</b>. 




<div class="alert"><b>Note</b>  When processing the data returned, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following table shows the error codes most commonly returned by the 
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
If the buffer specified by the <i>pbDecoded</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code, and stores the required buffer size, in bytes, in the variable pointed to by <i>pcbDecoded</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid message and certificate encoding types. Currently only PKCS_7_ASN_ENCODING and X509_ASN_ENCODING_TYPE are supported. Invalid <b>cbSize</b> in *<i>pVerifyPara</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNEXPECTED_MSG_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Not a signed cryptographic message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NO_SIGNER</b></dt>
</dl>
</td>
<td width="60%">
The message does not have any signers or a signer for the specified <i>dwSignerIndex</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The message was hashed and signed by using an unknown or unsupported algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
The message's signature was not verified.

</td>
</tr>
</table>