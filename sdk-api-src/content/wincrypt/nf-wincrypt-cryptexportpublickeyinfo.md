---
UID: NF:wincrypt.CryptExportPublicKeyInfo
title: CryptExportPublicKeyInfo function (wincrypt.h)
description: The CryptExportPublicKeyInfo function exports the public key information associated with the corresponding private key of the provider. For an updated version of this function, see CryptExportPublicKeyInfoEx.
helpviewer_keywords: ["CryptExportPublicKeyInfo","CryptExportPublicKeyInfo function [Security]","_crypto2_cryptexportpublickeyinfo","security.cryptexportpublickeyinfo","wincrypt/CryptExportPublicKeyInfo"]
old-location: security\cryptexportpublickeyinfo.htm
tech.root: security
ms.assetid: ad43a991-aaf5-4272-abab-0a981112e5e4
ms.date: 12/05/2018
ms.keywords: CryptExportPublicKeyInfo, CryptExportPublicKeyInfo function [Security], _crypto2_cryptexportpublickeyinfo, security.cryptexportpublickeyinfo, wincrypt/CryptExportPublicKeyInfo
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
 - CryptExportPublicKeyInfo
 - wincrypt/CryptExportPublicKeyInfo
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
 - CryptExportPublicKeyInfo
---

# CryptExportPublicKeyInfo function


## -description

The <b>CryptExportPublicKeyInfo</b> function exports the <a href="/windows/desktop/SecGloss/p-gly">public key</a> information associated with the corresponding <a href="/windows/desktop/SecGloss/p-gly">private key</a> of the provider. For an updated version of this function, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportpublickeyinfoex">CryptExportPublicKeyInfoEx</a>.

## -parameters

### -param hCryptProvOrNCryptKey [in]

Handle of the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) to use when exporting the public key information. This handle must be an <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a> handle that has been created by using the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> function or an <b>NCRYPT_KEY_HANDLE</b> handle that has been created by using the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptopenkey">NCryptOpenKey</a> function. New applications should always pass in the <b>NCRYPT_KEY_HANDLE</b> handle of a CNG CSP.

### -param dwKeySpec [in]

Identifies the private key to use from the container of the provider. It can be AT_KEYEXCHANGE or AT_SIGNATURE. This parameter is ignored if an <b>NCRYPT_KEY_HANDLE</b> is used in the <i>hCryptProvOrNCryptKey</i> parameter.

### -param dwCertEncodingType [in]

Specifies the <a href="/windows/desktop/SecGloss/e-gly">encoding type</a> used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pInfo [out]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a>  structure to receive the public key information to be exported.

To set the size of this information for memory allocation purposes, this parameter can be <b>NULL</b>. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbInfo [in, out]

A pointer to a <b>DWORD</b> that contains the size, in bytes, of the buffer pointed to by the <i>pInfo</i> parameter. When the function returns, the <b>DWORD</b> contains the number of bytes needed for the return buffer.

<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications need to use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetuserkey">CryptGetUserKey</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportkey">CryptExportKey</a> might be propagated to this function.</div>
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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pInfo</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code, and stores the required buffer size, in bytes, into the variable pointed to by <i>pcbInfo</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Invalid certificate encoding type. Currently only X509_ASN_ENCODING is supported.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportpublickeyinfo">CryptImportPublicKeyInfo</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>