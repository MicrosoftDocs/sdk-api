---
UID: NF:wincrypt.CryptExportPKCS8
title: CryptExportPKCS8 function (wincrypt.h)
description: Exports the private key in PKCS (CryptExportPKCS8)
helpviewer_keywords: ["AT_KEYEXCHANGE","AT_SIGNATURE","CryptExportPKCS8","CryptExportPKCS8 function [Security]","security.cryptexportpkcs8","wincrypt/CryptExportPKCS8"]
old-location: security\cryptexportpkcs8.htm
tech.root: security
ms.assetid: defd0b23-d9c2-4b28-a6a6-1be7487ae656
ms.date: 12/05/2018
ms.keywords: AT_KEYEXCHANGE, AT_SIGNATURE, CryptExportPKCS8, CryptExportPKCS8 function [Security], security.cryptexportpkcs8, wincrypt/CryptExportPKCS8
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
 - CryptExportPKCS8
 - wincrypt/CryptExportPKCS8
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
 - CryptExportPKCS8
---

# CryptExportPKCS8 function


## -description

<p class="CCE_Message">[The <b>CryptExportPKCS8</b>  function is no longer available for use as of Windows Server 2008 and Windows Vista. Instead, use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-pfxexportcertstoreex">PFXExportCertStoreEx</a> function.]

The <b>CryptExportPKCS8</b> function exports the <a href="/windows/desktop/SecGloss/p-gly">private key</a> in PKCS #8 format. The function is superseded by <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportpkcs8ex">CryptExportPKCS8Ex</a>, which also may be altered or unavailable in subsequent versions.

## -parameters

### -param hCryptProv [in]

An <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a>  variable that contains  the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP). This is a handle to the CSP obtained by calling <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>.

### -param dwKeySpec [in]

A <b>DWORD</b>  variable that contains  the key specification. The following <i>dwKeySpec</i> values are defined for the default provider.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AT_KEYEXCHANGE"></a><a id="at_keyexchange"></a><dl>
<dt><b>AT_KEYEXCHANGE</b></dt>
</dl>
</td>
<td width="60%">
Keys used to encrypt/decrypt session keys.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_SIGNATURE"></a><a id="at_signature"></a><dl>
<dt><b>AT_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
Keys used to create and verify digital signatures.

</td>
</tr>
</table>

### -param pszPrivateKeyObjId [in]

An  <b>LPSTR</b>  variable that contains  the private key <a href="/windows/desktop/SecGloss/o-gly"> object identifier</a> (OID).

### -param dwFlags [in]

This parameter should be zero if <i>pbPrivateKeyBlob</i> is <b>NULL</b> and 0x8000 otherwise.

### -param pvAuxInfo [in, optional]

This parameter must be set to <b>NULL</b>.

### -param pbPrivateKeyBlob [out, optional]

A pointer to an 
array of <b>BYTE</b> structures to receive the private key  to be exported. 


The private key will contain the information in a PKCS #8 PrivateKeyInfo <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) type found in the PKCS #8 standard.

For memory allocation purposes, you can get the size of the private key  to be exported by setting this parameter to <b>NULL</b>. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbPrivateKeyBlob [in, out]

A pointer to a <b>DWORD</b> that may contain, on input, the size, in  bytes,  of the memory allocation needed to contain the <i>pbPrivateKeyBlob</i>. If <i>pbPrivateKeyBlob</i> is <b>NULL</b>, this parameter will return the size of the memory allocation needed for a second call to the function. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. For extended error information, call 
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
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>  may return an ASN.1 encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -remarks

This function is only supported for asymmetric keys.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportpkcs8ex">CryptExportPKCS8Ex</a>



<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>
