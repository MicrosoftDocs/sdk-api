---
UID: NF:wincrypt.CryptVerifyMessageSignature
title: CryptVerifyMessageSignature function (wincrypt.h)
description: Verifies a signed message's signature.
helpviewer_keywords: ["CryptVerifyMessageSignature","CryptVerifyMessageSignature function [Security]","_crypto2_cryptverifymessagesignature","security.cryptverifymessagesignature","wincrypt/CryptVerifyMessageSignature"]
old-location: security\cryptverifymessagesignature.htm
tech.root: security
ms.assetid: 03411e7a-b097-4059-a198-3d412ae40e38
ms.date: 12/05/2018
ms.keywords: CryptVerifyMessageSignature, CryptVerifyMessageSignature function [Security], _crypto2_cryptverifymessagesignature, security.cryptverifymessagesignature, wincrypt/CryptVerifyMessageSignature
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
 - CryptVerifyMessageSignature
 - wincrypt/CryptVerifyMessageSignature
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
 - CryptVerifyMessageSignature
---

# CryptVerifyMessageSignature function


## -description

The <b>CryptVerifyMessageSignature</b> function verifies a signed message's signature.

This function should not be used to verify the signature of a detached message. You should use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifydetachedmessagesignature">CryptVerifyDetachedMessageSignature</a> function to verify the signature of a detached message.

## -parameters

### -param pVerifyPara [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_verify_message_para">CRYPT_VERIFY_MESSAGE_PARA</a> structure that contains verification parameters.

### -param dwSignerIndex [in]

The index of the desired signature. There can be more than one signature. <b>CryptVerifyMessageSignature</b> can be called repeatedly, incrementing <i>dwSignerIndex</i> each time. Set this parameter to zero for the first signer, or if there is only one signer. If the function returns <b>FALSE</b>, and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns CRYPT_E_NO_SIGNER, the previous call processed the last signer of the message.

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

### -param ppSignerCert [out, optional]

The address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure pointer that receives the certificate of the signer. When you have finished using this structure, free it by passing this pointer to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> function. This parameter can be <b>NULL</b> if the signer's certificate is not needed.

## -returns

If the function succeeds, the function returns nonzero. This does not necessarily mean that the signature was verified. In the case of a detached message, the variable pointed to by <i>pcbDecoded</i> will contain zero. In this case, this function will return nonzero, but the signature is not verified. To verify the signature of a detached message, use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifydetachedmessagesignature">CryptVerifyDetachedMessageSignature</a> function.

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
 

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a>, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifysignaturea">CryptVerifySignature</a>, and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a> can be propagated to this function. <p class="note">If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>. 

</div>
<div> </div>

## -remarks

For a verified signer and message, <i>ppSignerCert</i> is updated with the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> of the signer. It must be freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>. Otherwise, <i>ppSignerCert</i> is set to <b>NULL</b>.

For a message that contains only certificates and <a href="/windows/desktop/SecGloss/c-gly">CRLs</a>, <i>pcbDecoded</i> is set to <b>NULL</b>.


#### Examples

For an example that uses this function, see 
<a href="/windows/desktop/SecCrypto/example-c-program-signing-a-message-and-verifying-a-message-signature">Example C Program: Signing a Message and Verifying a Message Signature</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignmessage">CryptSignMessage</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifydetachedmessagesignature">CryptVerifyDetachedMessageSignature</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>