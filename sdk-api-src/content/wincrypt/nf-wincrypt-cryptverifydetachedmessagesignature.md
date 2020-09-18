---
UID: NF:wincrypt.CryptVerifyDetachedMessageSignature
title: CryptVerifyDetachedMessageSignature function (wincrypt.h)
description: The CryptVerifyDetachedMessageSignature function verifies a signed message containing a detached signature or signatures.
helpviewer_keywords: ["CryptVerifyDetachedMessageSignature","CryptVerifyDetachedMessageSignature function [Security]","_crypto2_cryptverifydetachedmessagesignature","security.cryptverifydetachedmessagesignature","wincrypt/CryptVerifyDetachedMessageSignature"]
old-location: security\cryptverifydetachedmessagesignature.htm
tech.root: security
ms.assetid: d437f6bf-eb56-4d29-bb91-eb8487e50219
ms.date: 12/05/2018
ms.keywords: CryptVerifyDetachedMessageSignature, CryptVerifyDetachedMessageSignature function [Security], _crypto2_cryptverifydetachedmessagesignature, security.cryptverifydetachedmessagesignature, wincrypt/CryptVerifyDetachedMessageSignature
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
 - CryptVerifyDetachedMessageSignature
 - wincrypt/CryptVerifyDetachedMessageSignature
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
 - CryptVerifyDetachedMessageSignature
---

# CryptVerifyDetachedMessageSignature function


## -description

The <b>CryptVerifyDetachedMessageSignature</b> function verifies a signed message containing a detached signature or signatures.

## -parameters

### -param pVerifyPara [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_verify_message_para">CRYPT_VERIFY_MESSAGE_PARA</a> structure containing the verification parameters.

### -param dwSignerIndex [in]

Index of the signature to be verified. A message might have several signers and this function can be called repeatedly, changing <i>dwSignerIndex</i> to verify other signatures. If the function returns FALSE, and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns CRYPT_E_NO_SIGNER, the previous call received the last signer of the message.

### -param pbDetachedSignBlob [in]

A pointer to a BLOB containing the encoded message signatures.

### -param cbDetachedSignBlob [in]

The size, in bytes, of the detached signature.

### -param cToBeSigned [in]

Number of array elements in <i>rgpbToBeSigned</i> and <i>rgcbToBeSigned</i>.

### -param rgpbToBeSigned [in]

Array of pointers to buffers containing the contents to be <a href="/windows/desktop/SecGloss/h-gly">hashed</a>.

### -param rgcbToBeSigned [in]

Array of sizes, in bytes, for the content buffers pointed to in <i>rgpbToBeSigned</i>.

### -param ppSignerCert [out, optional]

A pointer to a 
pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure of a signer certificate. When you have finished using the certificate context, free it by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> function. A pointer to a <b>CERT_CONTEXT</b> structure will not be returned if this parameter is <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (<b>FALSE</b>).

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
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a> might be propagated to this function.<p class="note">If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>. 

</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifymessagesignature">CryptVerifyMessageSignature</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>