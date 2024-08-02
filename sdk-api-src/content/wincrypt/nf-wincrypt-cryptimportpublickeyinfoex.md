---
UID: NF:wincrypt.CryptImportPublicKeyInfoEx
title: CryptImportPublicKeyInfoEx function (wincrypt.h)
description: Important  This API is deprecated. (CryptImportPublicKeyInfoEx)
helpviewer_keywords: ["CryptImportPublicKeyInfoEx","CryptImportPublicKeyInfoEx function [Security]","_crypto2_cryptimportpublickeyinfoex","security.cryptimportpublickeyinfoex","wincrypt/CryptImportPublicKeyInfoEx"]
old-location: security\cryptimportpublickeyinfoex.htm
tech.root: security
ms.assetid: d3a59f83-c761-46bb-ac4f-f42f689ea5f1
ms.date: 12/05/2018
ms.keywords: CryptImportPublicKeyInfoEx, CryptImportPublicKeyInfoEx function [Security], _crypto2_cryptimportpublickeyinfoex, security.cryptimportpublickeyinfoex, wincrypt/CryptImportPublicKeyInfoEx
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
 - CryptImportPublicKeyInfoEx
 - wincrypt/CryptImportPublicKeyInfoEx
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
 - CryptImportPublicKeyInfoEx
---

# CryptImportPublicKeyInfoEx function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptImportPublicKeyInfoEx</b> function imports public key information into the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) and returns a handle of the public key. Additional parameters to override defaults are provided to supplement those in 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a>.

## -parameters

### -param hCryptProv [in]

The handle of the CSP to receive the imported public key. This handle must have already been created using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>.

### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pInfo [in]

the address of a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure that contains the public key to import into the provider.

<div class="alert"><b>Note</b>  The <b>pzObjId</b> member of the <b>Algorithm</b> member pointed to by the <i>pInfo</i>  and <i>dwCertEncodingType</i> parameters determine an installable <b>CRYPT_OID_IMPORT_PUBLIC_KEY_INFO_FUNC</b> callback function. If an installable function is not found, an attempt is made to import the key as an RSA Public Key (szOID_RSA_RSA).</div>
<div> </div>

### -param aiKeyAlg [in]

An <a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a> structure that contains a CSP-specific algorithm to override the <a href="/windows/desktop/SecGloss/c-gly">CALG_RSA_KEYX</a> default algorithm.

### -param dwFlags [in]

Reserved for future use and must be zero.

### -param pvAuxInfo [in]

Reserved for future use and must be <b>NULL</b>.

### -param phKey [out]

The address of an <b>HCRYPTKEY</b> variable that receives the handle of the imported public key. When you have finished using the public key, release the handle by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdestroykey">CryptDestroyKey</a> function.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetuserkey">CryptGetUserKey</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportkey">CryptExportKey</a> might be propagated to this function. This function has the following error code.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
An import function that can be installed or registered could not be found for the specified <i>dwCertEncodingType</i> and <i>pInfo</i> parameters.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -remarks

This function is normally used to retrieve the public key from a certificate. This is done by passing the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure from a filled-in certificate structure as shown in the following pseudocode.


``` syntax
PCCERT_CONTEXT pCertContext

// Get the certificate context structure from a certificate.
pCertContext = CertCreateCertificateContext(...)
if(pCertContext)
{
    HCRYPTKEY hCertPubKey

    // Get the public key information for the certificate.
    CryptImportPublicKeyInfo(
        hCryptProv, 
        X509_ASN_ENCODING, 
        &pCertContext->pCertInfo->SubjectPublicKeyInfo, 
        &hCertPubKey)

    CertFreeCertificateContext(pCertContext)
}
```


## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportpublickeyinfoex">CryptExportPublicKeyInfoEx</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>
