---
UID: NF:wincrypt.CryptMsgVerifyCountersignatureEncoded
title: CryptMsgVerifyCountersignatureEncoded function (wincrypt.h)
description: Verifies a countersignature in terms of the SignerInfo structure (as defined by PKCS
helpviewer_keywords: ["CryptMsgVerifyCountersignatureEncoded","CryptMsgVerifyCountersignatureEncoded function [Security]","_crypto2_cryptmsgverifycountersignatureencoded","security.cryptmsgverifycountersignatureencoded","wincrypt/CryptMsgVerifyCountersignatureEncoded"]
old-location: security\cryptmsgverifycountersignatureencoded.htm
tech.root: security
ms.assetid: b0332360-a737-4b48-b592-0c55d493a02d
ms.date: 12/05/2018
ms.keywords: CryptMsgVerifyCountersignatureEncoded, CryptMsgVerifyCountersignatureEncoded function [Security], _crypto2_cryptmsgverifycountersignatureencoded, security.cryptmsgverifycountersignatureencoded, wincrypt/CryptMsgVerifyCountersignatureEncoded
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - CryptMsgVerifyCountersignatureEncoded
 - wincrypt/CryptMsgVerifyCountersignatureEncoded
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
 - CryptMsgVerifyCountersignatureEncoded
---

# CryptMsgVerifyCountersignatureEncoded function


## -description

The <b>CryptMsgVerifyCountersignatureEncoded</b> function verifies a <a href="/windows/desktop/SecGloss/c-gly">countersignature</a> in terms of the SignerInfo structure (as defined by PKCS #7).

## -parameters

### -param hCryptProv [in]

This parameter is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b><b>NULL</b> or the handle of the <a href="/windows/desktop/SecGloss/c-gly">cryptographic provider</a> to use to <a href="/windows/desktop/SecGloss/h-gly">hash</a> the encryptedDigest field of <i>pbSignerInfo</i>.This parameter's data type is <b>HCRYPTPROV</b>.

Unless there is a strong reason for passing in a specific cryptographic provider in <i>hCryptProv</i>, pass <b>NULL</b> to cause the default RSA or DSS provider to be used.

### -param dwEncodingType [in]

Specifies the encoding type used. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. For either current encoding type, use: 


X509_ASN_ENCODING | PKCS_7_ASN_ENCODING.

### -param pbSignerInfo [in]

A pointer to the encoded <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> that contains the signer of the contents of a message to be countersigned.

### -param cbSignerInfo [in]

Count, in bytes, of the encoded BLOB for the signer of the contents.

### -param pbSignerInfoCountersignature [in]

A pointer to the encoded BLOB containing the countersigner information.

### -param cbSignerInfoCountersignature [in]

Count, in bytes, of the encoded BLOB for the countersigner of the message.

### -param pciCountersigner [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> that includes with the issuer and serial number of the countersigner. For more information, see Remarks.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following table lists the error codes most commonly returned by the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_AUTH_ATTR_MISSING</b></dt>
</dl>
</td>
<td width="60%">
The message does not contain an expected authenticated attribute.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_HASH_VALUE</b></dt>
</dl>
</td>
<td width="60%">
The hash value is not correct.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNEXPECTED_ENCODING</b></dt>
</dl>
</td>
<td width="60%">
The message is not encoded as expected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNKNOWN_ALGO</b></dt>
</dl>
</td>
<td width="60%">
The cryptographic algorithm is unknown.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Ran out of memory.

</td>
</tr>
</table>
 

Propagated errors from the following functions might be returned.

<ul>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgethashparam">CryptGetHashParam</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifysignaturea">CryptVerifySignature</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>
</li>
</ul>
If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -remarks

Countersigner verification is done using the PKCS #7 <b>SIGNERINFO</b> structure. The signature must contain the encrypted hash of the encryptedDigest field of <i>pbSignerInfo</i>.

The issuer and serial number of the countersigner must match the countersigner information from <i>pbSignerInfoCountersignature</i>. The only fields referenced from <i>pciCountersigner</i> are SerialNumber, Issuer, and SubjectPublicKeyInfo. The SubjectPublicKeyInfo is used to access the public key that is then used to encrypt the <a href="/windows/desktop/SecGloss/h-gly">hash</a> from the <i>pciCountersigner</i> so compare it with the hash from the <i>pbSignerInfo</i>.


#### Examples

For an example that uses this function, see 
<a href="/windows/desktop/SecCrypto/example-c-program-encoding-and-decoding-a-countersigned-message">Example C Program: Encoding and Decoding a CounterSigned Message</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcountersign">CryptMsgCountersign</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcountersignencoded">CryptMsgCountersignEncoded</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Low-level Message Functions</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>