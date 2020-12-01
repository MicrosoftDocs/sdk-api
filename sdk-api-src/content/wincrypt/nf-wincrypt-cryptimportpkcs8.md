---
UID: NF:wincrypt.CryptImportPKCS8
title: CryptImportPKCS8 function (wincrypt.h)
description: Imports the private key in PKCS
helpviewer_keywords: ["CRYPT_EXPORTABLE","CRYPT_USER_PROTECTED","CryptImportPKCS8","CryptImportPKCS8 function [Security]","security.cryptimportpkcs8","wincrypt/CryptImportPKCS8"]
old-location: security\cryptimportpkcs8.htm
tech.root: security
ms.assetid: fa3deff9-b4c1-4b63-a59f-738f87e1a409
ms.date: 12/05/2018
ms.keywords: CRYPT_EXPORTABLE, CRYPT_USER_PROTECTED, CryptImportPKCS8, CryptImportPKCS8 function [Security], security.cryptimportpkcs8, wincrypt/CryptImportPKCS8
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
 - CryptImportPKCS8
 - wincrypt/CryptImportPKCS8
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
 - CryptImportPKCS8
---

# CryptImportPKCS8 function


## -description

<p class="CCE_Message">[The <b>CryptImportPKCS8</b> function is no longer available for use as of Windows Server 2008 and Windows Vista. Instead, use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore">PFXImportCertStore</a> function.]
<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptImportPKCS8</b> function imports the <a href="/windows/desktop/SecGloss/p-gly">private key</a> in PKCS #8 format to a <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP).<b>CryptImportPKCS8</b> will return a handle to the provider and the import KeySpec used.

## -parameters

### -param sPrivateKeyAndParams [in]

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_pkcs8_import_params">CRYPT_PKCS8_IMPORT_PARAMS</a> structure that contains the <a href="/windows/desktop/SecGloss/p-gly">private key BLOB</a> and corresponding parameters.

### -param dwFlags [in]

A  <b>DWORD</b>  value. This parameter can be one of the following values, a combination of them, or a null value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_EXPORTABLE"></a><a id="crypt_exportable"></a><dl>
<dt><b>CRYPT_EXPORTABLE</b></dt>
</dl>
</td>
<td width="60%">
The key being imported is eventually to be reexported. If this flag is not used, then calls to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportkey">CryptExportKey</a> with the key handle fail.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_USER_PROTECTED"></a><a id="crypt_user_protected"></a><dl>
<dt><b>CRYPT_USER_PROTECTED</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the CSP notifies the user through a dialog box or some other method when certain actions are attempted using this key. The precise behavior is specified by the CSP or the CSP type used. 
If the provider context was acquired with CRYPT_SILENT set, using this flag causes a failure, and the last error is set to NTE_SILENT_CONTEXT.

</td>
</tr>
</table>

### -param phCryptProv [out, optional]

A pointer to the <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a>  to receive the handle of the provider into which the key is
imported by calling the <b>CryptImportPKCS8</b> function.  

When you have finished using the handle, free the handle by calling <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptreleasecontext">CryptReleaseContext</a>. 

This parameter can be <b>NULL</b>, in which case the handle of the provider is not returned.

### -param pvAuxInfo [in, optional]

This parameter must be <b>NULL</b>.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following error code is specific to this function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNSUPPORTED_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The algorithm <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of the private
      key is not supported.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>  may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -remarks

<b>CryptImportPKCS8</b>  calls the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pcrypt_resolve_hcryptprov_func">PCRYPT_RESOLVE_HCRYPTPROV_FUNC</a> function  by using the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_pkcs8_import_params">CRYPT_PKCS8_IMPORT_PARAMS</a> structure contained in the <i>sPrivateKeyAndParams</i> parameter to retrieve a handle of the provider to which to import the key.  If  <b>PCRYPT_RESOLVE_HCRYPTPROV_FUNC</b> is <b>NULL</b>, then the default provider is used.

This function is only supported for asymmetric keys.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_pkcs8_import_params">CRYPT_PKCS8_IMPORT_PARAMS</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportpkcs8ex">CryptExportPKCS8Ex</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptreleasecontext">CryptReleaseContext</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pcrypt_decrypt_private_key_func">PCRYPT_DECRYPT_PRIVATE_KEY_FUNC</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pcrypt_resolve_hcryptprov_func">PCRYPT_RESOLVE_HCRYPTPROV_FUNC</a>