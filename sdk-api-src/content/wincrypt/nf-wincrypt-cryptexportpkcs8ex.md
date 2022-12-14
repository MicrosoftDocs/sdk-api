---
UID: NF:wincrypt.CryptExportPKCS8Ex
title: CryptExportPKCS8Ex function (wincrypt.h)
description: Exports the private key in PKCS (CryptExportPKCS8Ex)
helpviewer_keywords: ["CryptExportPKCS8Ex","CryptExportPKCS8Ex function [Security]","security.cryptexportpkcs8ex","wincrypt/CryptExportPKCS8Ex"]
old-location: security\cryptexportpkcs8ex.htm
tech.root: security
ms.assetid: 82fee86a-8704-4f22-8f11-f89509c5a0aa
ms.date: 12/05/2018
ms.keywords: CryptExportPKCS8Ex, CryptExportPKCS8Ex function [Security], security.cryptexportpkcs8ex, wincrypt/CryptExportPKCS8Ex
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
req.lib: 
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptExportPKCS8Ex
 - wincrypt/CryptExportPKCS8Ex
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
 - CryptExportPKCS8Ex
---

# CryptExportPKCS8Ex function


## -description

<p class="CCE_Message">[The <b>CryptExportPKCS8Ex</b> function is no longer available for use as of Windows Server 2008 and Windows Vista. Instead, use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-pfxexportcertstoreex">PFXExportCertStoreEx</a> function.]

The <b>CryptExportPKCS8Ex</b> function exports the <a href="/windows/desktop/SecGloss/p-gly">private key</a> in PKCS #8 format.This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Crypt32.dll.

## -parameters

### -param psExportParams [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_pkcs8_export_params">CRYPT_PKCS8_EXPORT_PARAMS</a> structure that contains information about the key to export.

### -param dwFlags [in]

This parameter should be zero if <i>pbPrivateKeyBlob</i> is <b>NULL</b> and 0x8000 otherwise.

### -param pvAuxInfo [in, optional]

This parameter must be <b>NULL</b>.

### -param pbPrivateKeyBlob [out, optional]

A pointer to an 
array of <b>BYTE</b> structures to receive the private key  to be exported. 


The private key will contain the information in a PKCS #8
PrivateKeyInfo <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) type found in the PKCS #8 standard.

For memory allocation purposes, you can get the size of the private key  to be exported by setting this parameter to <b>NULL</b>. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbPrivateKeyBlob [in, out]

A pointer to a <b>DWORD</b> that may contain, on input, the size, in  bytes,  of the memory allocation needed to contain the <i>pbPrivateKeyBlob</i>. If <i>pbPrivateKeyBlob</i> is <b>NULL</b>, this parameter will return the size of the memory allocation needed for a second call to the function. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following error codes are specific to this function.

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
An export function that can be installed or registered could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pbPrivateKeyBlob</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, in the variable pointed to by the <i>pcbPrivateKeyBlob</i> parameter.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>   returns an ASN.1 encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -remarks

This function is only supported for asymmetric keys.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_pkcs8_export_params">CRYPT_PKCS8_EXPORT_PARAMS</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportpkcs8">CryptExportPKCS8</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportpkcs8">CryptImportPKCS8</a>
