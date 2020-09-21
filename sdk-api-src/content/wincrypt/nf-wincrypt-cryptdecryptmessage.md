---
UID: NF:wincrypt.CryptDecryptMessage
title: CryptDecryptMessage function (wincrypt.h)
description: The CryptDecryptMessage function decodes and decrypts a message.
helpviewer_keywords: ["CryptDecryptMessage","CryptDecryptMessage function [Security]","_crypto2_cryptdecryptmessage","security.cryptdecryptmessage","wincrypt/CryptDecryptMessage"]
old-location: security\cryptdecryptmessage.htm
tech.root: security
ms.assetid: e540b816-64e1-4c78-9020-2b221e813acc
ms.date: 12/05/2018
ms.keywords: CryptDecryptMessage, CryptDecryptMessage function [Security], _crypto2_cryptdecryptmessage, security.cryptdecryptmessage, wincrypt/CryptDecryptMessage
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
 - CryptDecryptMessage
 - wincrypt/CryptDecryptMessage
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
 - CryptDecryptMessage
---

# CryptDecryptMessage function


## -description

The <b>CryptDecryptMessage</b> function <a href="/windows/desktop/SecGloss/d-gly">decodes</a> and <a href="/windows/desktop/SecGloss/d-gly">decrypts</a> a message.

## -parameters

### -param pDecryptPara [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_decrypt_message_para">CRYPT_DECRYPT_MESSAGE_PARA</a> structure that contains decryption parameters.

### -param pbEncryptedBlob [in]

A pointer to a buffer that contains the <a href="/windows/desktop/SecGloss/e-gly">encoded</a> and <a href="/windows/desktop/SecGloss/e-gly">encrypted</a> message to be decrypted.

### -param cbEncryptedBlob [in]

The size, in bytes, of the encoded and encrypted message.

### -param pbDecrypted [out, optional]

A pointer to a buffer that receives the decrypted message. 




To set the size of this information for memory allocation purposes, this parameter can be <b>NULL</b>. A decrypted message will not be returned if this parameter is <b>NULL</b>. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbDecrypted [in, out, optional]

A pointer to a <b>DWORD</b> that specifies the size, in bytes, of the buffer pointed to by the <i>pbDecrypted</i> parameter. When the function returns, this variable contains the size, in bytes, of the decrypted message copied to <i>pbDecrypted</i>.
						

<div class="alert"><b>Note</b>  When processing the data returned in the <i>pbDecrypted</i> buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified in <i>pcbDecrypted</i> on input. On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer. On output, the <b>DWORD</b> is updated to the actual size of the data copied to the buffer.</div>
<div> </div>

### -param ppXchgCert [out, optional]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure of a <a href="/windows/desktop/SecGloss/c-gly">certificate</a> that corresponds to the private <a href="/windows/desktop/SecGloss/e-gly">exchange key</a> needed to decrypt the message. To indicate that the function should not return the <a href="/windows/desktop/SecGloss/c-gly">certificate context</a> used to decrypt, set this parameter to <b>NULL</b>.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from calls to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecrypt">CryptDecrypt</a> might be propagated to this function.</div>
<div> </div>
The <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns the following error codes most often.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid message and <a href="/windows/desktop/SecGloss/c-gly">certificate encoding types</a>. Currently only PKCS_7_ASN_ENCODING and X509_ASN_ENCODING_TYPE are supported. Invalid <b>cbSize</b> in *<i>pDecryptPara</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNEXPECTED_MSG_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Not an <a href="/windows/desktop/SecGloss/e-gly">enveloped</a> cryptographic message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The message was encrypted by using an unknown or unsupported algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NO_DECRYPT_CERT</b></dt>
</dl>
</td>
<td width="60%">
No certificate was found having a <a href="/windows/desktop/SecGloss/p-gly">private key</a> property to use for decrypting.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -remarks

When <b>NULL</b> is passed for <i>pbDecrypted</i>, and <i>pcbDecrypted</i> is not <b>NULL</b>, <b>NULL</b> is returned for the address passed in <i>ppXchgCert</i>; otherwise, a pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> is returned. For a successfully decrypted message, this pointer to a <b>CERT_CONTEXT</b> points to the <a href="/windows/desktop/SecGloss/c-gly">certificate context</a> used to decrypt the message. It must be freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>. If the function fails, the value at <i>ppXchgCert</i> is set to <b>NULL</b>.


#### Examples

For an example that uses this function, see 
<a href="/windows/desktop/SecCrypto/example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage">Example C Program: Using CryptEncryptMessage and CryptDecryptMessage</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature">CryptDecryptAndVerifyMessageSignature</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>