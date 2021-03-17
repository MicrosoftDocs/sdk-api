---
UID: NC:wincrypt.PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC
title: PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC (wincrypt.h)
description: Called by CryptExportPublicKeyInfoEx to export a public key BLOB and encode it.
helpviewer_keywords: ["PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC","PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC callback","PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC callback function [Security]","security.pfn_crypt_export_public_key_info_ex2_func","wincrypt/PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC"]
old-location: security\pfn_crypt_export_public_key_info_ex2_func.htm
tech.root: security
ms.assetid: 37315539-64f8-4708-8a17-f80a2869e6b3
ms.date: 12/05/2018
ms.keywords: PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC, PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC callback, PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC callback function [Security], security.pfn_crypt_export_public_key_info_ex2_func, wincrypt/PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC
 - wincrypt/PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC
---

# PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC callback function


## -description

The <b>PFN_CRYPT_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC</b> callback function is called by <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportpublickeyinfoex">CryptExportPublicKeyInfoEx</a> to export a public key BLOB and encode it.

## -parameters

### -param hNCryptKey [in]

A handle of the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) to use when exporting the public key information. This handle must be an <b>NCRYPT_KEY_HANDLE</b> handle that has been created by using the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptopenkey">NCryptOpenKey</a> function.

### -param dwCertEncodingType [in]

A value that specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pszPublicKeyObjId [in]

A pointer to a string that contains the <a href="/windows/desktop/SecGloss/p-gly">public key algorithm</a>.

### -param dwFlags [in]

A value that indicates how the public key information  is exported. This can be zero.

### -param pvAuxInfo [in, optional]

This parameter is reserved for future use and  must be set to <b>NULL</b>.

### -param pInfo [out, optional]

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

If this callback function does not support the signature algorithm, it must return <b>FALSE</b> and call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> with <b>ERROR_NOT_SUPPORTED</b>.

## -remarks

You can use <a href="/windows/desktop/SecCrypto/cryptography-functions">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constant for this purpose.

<table>
<tr>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td>CRYPT_OID_EXPORT_PUBLIC_KEY_INFO_EX2_FUNC</td>
<td>"CryptDllExportPublicKeyInfoEx2"</td>
</tr>
</table>
