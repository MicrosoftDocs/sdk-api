---
UID: NF:wincrypt.CryptExportPublicKeyInfoEx
title: CryptExportPublicKeyInfoEx function (wincrypt.h)
description: Exports the public key information associated with the provider's corresponding private key.
helpviewer_keywords: ["CryptExportPublicKeyInfoEx","CryptExportPublicKeyInfoEx function [Security]","_crypto2_cryptexportpublickeyinfoex","security.cryptexportpublickeyinfoex","wincrypt/CryptExportPublicKeyInfoEx"]
old-location: security\cryptexportpublickeyinfoex.htm
tech.root: security
ms.assetid: 38274222-90b3-4038-86d3-6b2813100ce2
ms.date: 12/05/2018
ms.keywords: CryptExportPublicKeyInfoEx, CryptExportPublicKeyInfoEx function [Security], _crypto2_cryptexportpublickeyinfoex, security.cryptexportpublickeyinfoex, wincrypt/CryptExportPublicKeyInfoEx
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
 - CryptExportPublicKeyInfoEx
 - wincrypt/CryptExportPublicKeyInfoEx
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
 - CryptExportPublicKeyInfoEx
---

# CryptExportPublicKeyInfoEx function


## -description

The <b>CryptExportPublicKeyInfoEx</b> function exports the <a href="/windows/desktop/SecGloss/p-gly">public key</a> information associated with the provider's corresponding <a href="/windows/desktop/SecGloss/p-gly">private key</a>. This function allows the application to specify the <a href="/windows/desktop/SecGloss/p-gly">public key algorithm</a>, overriding the default provided by the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP).

## -parameters

### -param hCryptProvOrNCryptKey [in]

A handle of the CSP to use when exporting the public key information. This handle must be an <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a> handle that has been created by using the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> function or an <b>NCRYPT_KEY_HANDLE</b> handle that has been created by using the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptopenkey">NCryptOpenKey</a> function. New applications should always pass in the <b>NCRYPT_KEY_HANDLE</b> handle of a CNG CSP.

### -param dwKeySpec [in]

Identifies the <a href="/windows/desktop/SecGloss/p-gly">private key</a> to use from the provider's container. It can be AT_KEYEXCHANGE or AT_SIGNATURE. This parameter is ignored if an <b>NCRYPT_KEY_HANDLE</b> is used in the <i>hCryptProvOrNCryptKey</i> parameter.

### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pszPublicKeyObjId [in]

Specifies the public key algorithm.

<div class="alert"><b>Note</b>  <i>pszPublicKeyObjId</i> and <i>dwCertEncodingType</i> are used together to determine the installable <b>CRYPT_OID_EXPORT_PUBLIC_KEY_INFO_FUNC</b> to call. If an installable function was not found for the <i>pszPublicKeyObjId</i> parameter, an attempt is made to export the key as an RSA Public Key (szOID_RSA_RSA).</div>
<div> </div>

### -param dwFlags [in]

A <b>DWORD</b> flag value that indicates how the public key information  is exported. The flag value is passed directly to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo">CryptFindOIDInfo</a> function when mapping the public key <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> to the corresponding CNG public key algorithm Unicode string. The following flag values can be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG</dt>
</dl>
</td>
<td width="60%">
Skips public keys in the <b>CRYPT_PUBKEY_ALG_OID_GROUP_ID</b> group explicitly flagged with the <b>CRYPT_OID_PUBKEY_ENCRYPT_ONLY_FLAG</b> flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG</dt>
</dl>
</td>
<td width="60%">
Skips public keys in the <b>CRYPT_PUBKEY_ALG_OID_GROUP_ID</b> group explicitly flagged with the <b>CRYPT_OID_PUBKEY_SIGN_ONLY_FLAG</b> flag.

</td>
</tr>
</table>

### -param pvAuxInfo [in]

This parameter is reserved for future use and  must be set to <b>NULL</b>.

### -param pInfo [out]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a>  structure to receive the public key information to be exported.

This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbInfo [in, out]

A pointer to a <b>DWORD</b> that contains the size, in bytes, of the buffer pointed to by the <i>pInfo</i> parameter. When the function returns, the <b>DWORD</b> contains the number of bytes stored in the buffer.

<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications need to use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetuserkey">CryptGetUserKey</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportkey">CryptExportKey</a> can be propagated to this function.</div>
<div> </div>
This function has the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
An export function that can be installed or registered could not be found for the specified <i>dwCertEncodingType</i> and <i>pszPublicKeyObjId</i> parameters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pInfo</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, in the variable pointed to by the <i>pcbInfo</i> parameter.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportpublickeyinfoex">CryptImportPublicKeyInfoEx</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>