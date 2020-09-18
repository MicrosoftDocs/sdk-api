---
UID: NF:wincrypt.CryptDecryptAndVerifyMessageSignature
title: CryptDecryptAndVerifyMessageSignature function (wincrypt.h)
description: The CryptDecryptAndVerifyMessageSignature function decrypts a message and verifies its signature.
helpviewer_keywords: ["CryptDecryptAndVerifyMessageSignature","CryptDecryptAndVerifyMessageSignature function [Security]","_crypto2_cryptdecryptandverifymessagesignature","security.cryptdecryptandverifymessagesignature","wincrypt/CryptDecryptAndVerifyMessageSignature"]
old-location: security\cryptdecryptandverifymessagesignature.htm
tech.root: security
ms.assetid: 0864a187-617f-4a21-9809-d2dbbc54ab9c
ms.date: 12/05/2018
ms.keywords: CryptDecryptAndVerifyMessageSignature, CryptDecryptAndVerifyMessageSignature function [Security], _crypto2_cryptdecryptandverifymessagesignature, security.cryptdecryptandverifymessagesignature, wincrypt/CryptDecryptAndVerifyMessageSignature
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
 - CryptDecryptAndVerifyMessageSignature
 - wincrypt/CryptDecryptAndVerifyMessageSignature
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
 - CryptDecryptAndVerifyMessageSignature
---

# CryptDecryptAndVerifyMessageSignature function


## -description

The <b>CryptDecryptAndVerifyMessageSignature</b> function decrypts a message and verifies its signature.

## -parameters

### -param pDecryptPara [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_decrypt_message_para">CRYPT_DECRYPT_MESSAGE_PARA</a> structure that contains decryption parameters.

### -param pVerifyPara [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_verify_message_para">CRYPT_VERIFY_MESSAGE_PARA</a> structure that contains  verification parameters.

### -param dwSignerIndex [in]

Identifies a particular signer of the message. A message can be signed by more than one signer and this function can be called multiple times changing this parameter to check for several signers. It is set to zero for the first signer. If the function returns <b>FALSE</b>, and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns CRYPT_E_NO_SIGNER, the previous call received the last signer of the message.

### -param pbEncryptedBlob [in]

A pointer to the signed, encoded, and encrypted message to be decrypted and verified.

### -param cbEncryptedBlob [in]

The size, in bytes, of the encrypted message.

### -param pbDecrypted [out, optional]

A pointer to a buffer to receive the decrypted message. 




This parameter can be <b>NULL</b> if the decrypted message is not required or to set the size of the decrypted message for memory allocation purposes. A decrypted message will not be returned if this parameter is <b>NULL</b>. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbDecrypted [in, out, optional]

A pointer to a <b>DWORD</b> that specifies the size, in bytes, of the buffer pointed to by the <i>pbDecrypted</i> parameter. When the function returns, it contains the size of the decrypted message copied to <i>pbDecrypted</i>. 




<div class="alert"><b>Note</b>  When processing the data returned in the <i>pbDecrypted</i> buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified in <i>pcbDecrypted</i> on input. On output, the variable pointed to by this parameter is set to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

### -param ppXchgCert [out, optional]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure of the <a href="/windows/desktop/SecGloss/c-gly">certificate</a> that corresponds to the private <a href="/windows/desktop/SecGloss/e-gly">exchange key</a> needed to decrypt the message.

### -param ppSignerCert [out, optional]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure of the certificate of the signer.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecryptmessage">CryptDecryptMessage</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifymessagesignature">CryptVerifyMessageSignature</a> might be propagated to this function.</div>
<div> </div>
The <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns the following error code most often.

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
If the buffer specified by the <i>pbDecrypted</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code, and stores the required buffer size, in bytes, in the variable pointed to by <i>pcbDecrypted</i>.

</td>
</tr>
</table>

## -remarks

For a successfully <a href="/windows/desktop/SecGloss/d-gly">decrypted</a> and verified message, the <a href="/windows/desktop/SecGloss/c-gly">certificate context</a> pointers pointed to by <i>ppXchgCert</i> and <i>ppSignerCert</i> are updated. They must be freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>. If the function fails, they are set to <b>NULL</b>.

To indicate that the caller is not interested in the exchange certificate or the signer <a href="/windows/desktop/SecGloss/c-gly">certificate context</a>, set the <i>ppXchgCert</i> and <i>ppSignerCert</i> parameters to <b>NULL</b>.


#### Examples

For an example that uses this function, see 
<a href="/windows/desktop/SecCrypto/example-c-program-sending-and-receiving-a-signed-and-encrypted-message">Example C Program: Sending and Receiving a Signed and Encrypted Message</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecryptmessage">CryptDecryptMessage</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignandencryptmessage">CryptSignAndEncryptMessage</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>