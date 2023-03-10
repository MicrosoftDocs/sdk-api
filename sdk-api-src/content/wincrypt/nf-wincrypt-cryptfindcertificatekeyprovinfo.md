---
UID: NF:wincrypt.CryptFindCertificateKeyProvInfo
title: CryptFindCertificateKeyProvInfo function (wincrypt.h)
description: Enumerates the cryptographic providers and their containers to find the private key that corresponds to the certificate's public key.
helpviewer_keywords: ["CRYPT_ACQUIRE_ALLOW_NCRYPT_KEY_FLAG","CRYPT_ACQUIRE_ONLY_NCRYPT_KEY_FLAG","CRYPT_ACQUIRE_PREFER_NCRYPT_KEY_FLAG","CRYPT_FIND_MACHINE_KEYSET_FLAG","CRYPT_FIND_SILENT_KEYSET_FLAG","CRYPT_FIND_USER_KEYSET_FLAG","CryptFindCertificateKeyProvInfo","CryptFindCertificateKeyProvInfo function [Security]","_crypto2_cryptfindcertificatekeyprovinfo","security.cryptfindcertificatekeyprovinfo","wincrypt/CryptFindCertificateKeyProvInfo"]
old-location: security\cryptfindcertificatekeyprovinfo.htm
tech.root: security
ms.assetid: 9e63517d-a56e-45a9-972c-de9a297e9e25
ms.date: 12/05/2018
ms.keywords: CRYPT_ACQUIRE_ALLOW_NCRYPT_KEY_FLAG, CRYPT_ACQUIRE_ONLY_NCRYPT_KEY_FLAG, CRYPT_ACQUIRE_PREFER_NCRYPT_KEY_FLAG, CRYPT_FIND_MACHINE_KEYSET_FLAG, CRYPT_FIND_SILENT_KEYSET_FLAG, CRYPT_FIND_USER_KEYSET_FLAG, CryptFindCertificateKeyProvInfo, CryptFindCertificateKeyProvInfo function [Security], _crypto2_cryptfindcertificatekeyprovinfo, security.cryptfindcertificatekeyprovinfo, wincrypt/CryptFindCertificateKeyProvInfo
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
 - CryptFindCertificateKeyProvInfo
 - wincrypt/CryptFindCertificateKeyProvInfo
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
 - CryptFindCertificateKeyProvInfo
---

# CryptFindCertificateKeyProvInfo function


## -description

The <b>CryptFindCertificateKeyProvInfo</b> function enumerates the <a href="/windows/desktop/SecGloss/c-gly">cryptographic providers</a> and their containers to find the <a href="/windows/desktop/SecGloss/p-gly">private key</a> that corresponds to the certificate's <a href="/windows/desktop/SecGloss/p-gly">public key</a>.

## -parameters

### -param pCert [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure of the certificate to use when exporting public key information.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. This can be zero or one of the following values.
						
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_FIND_USER_KEYSET_FLAG"></a><a id="crypt_find_user_keyset_flag"></a><dl>
<dt><b>CRYPT_FIND_USER_KEYSET_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Restricts the search to the user container. The default is to search both the user and machine containers.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_FIND_MACHINE_KEYSET_FLAG"></a><a id="crypt_find_machine_keyset_flag"></a><dl>
<dt><b>CRYPT_FIND_MACHINE_KEYSET_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Restricts the search to the machine container. The default is to search both the user and machine containers.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_FIND_SILENT_KEYSET_FLAG"></a><a id="crypt_find_silent_keyset_flag"></a><dl>
<dt><b>CRYPT_FIND_SILENT_KEYSET_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The application requests that the CSP not display any user interface (UI) for this context. If the CSP must display the UI to operate, the call fails and the NTE_SILENT_CONTEXT error code is set as the last error.

</td>
</tr>
</table>
 


The following flags determine which technology is used to obtain the key. If none of these flags is present, this function will only attempt to obtain the key by using CryptoAPI.

<b>Windows Server 2003 and Windows XP:  </b>These flags are not supported.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ACQUIRE_ALLOW_NCRYPT_KEY_FLAG"></a><a id="crypt_acquire_allow_ncrypt_key_flag"></a><dl>
<dt><b>CRYPT_ACQUIRE_ALLOW_NCRYPT_KEY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
This function will attempt to obtain the key by using CryptoAPI. If that fails, this function will attempt to obtain the key by using the Cryptography API:  Next Generation (CNG). 

The <b>CERT_KEY_PROV_INFO_PROP_ID</b> property of the certificate is set to zero if CNG is used to obtain the key.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ACQUIRE_ONLY_NCRYPT_KEY_FLAG_"></a><a id="crypt_acquire_only_ncrypt_key_flag_"></a><dl>
<dt><b>CRYPT_ACQUIRE_ONLY_NCRYPT_KEY_FLAG
</b></dt>
</dl>
</td>
<td width="60%">
This function will only attempt to obtain the key by using CNG and will not use CryptoAPI to obtain the key. 

The <b>CERT_KEY_PROV_INFO_PROP_ID</b> property of the certificate is set to zero if CNG is used to obtain the key.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ACQUIRE_PREFER_NCRYPT_KEY_FLAG"></a><a id="crypt_acquire_prefer_ncrypt_key_flag"></a><dl>
<dt><b>CRYPT_ACQUIRE_PREFER_NCRYPT_KEY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
This function will attempt to obtain the key by using CNG. If that fails, this function will attempt to obtain the key by using CryptoAPI. 

The <b>CERT_KEY_PROV_INFO_PROP_ID</b> property of the certificate is set to zero if CNG is used to obtain the key.

</td>
</tr>
</table>

### -param pvReserved [in]

Reserved for future use and must be <b>NULL</b>.

## -returns

<b>TRUE</b> if the function finds a private key that corresponds to the certificate's public key within a searched <a href="/windows/desktop/SecGloss/k-gly">container</a>; <b>FALSE</b> if the function fails to find a container or a private key within a container.


<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns the following error:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_KEY</b></dt>
</dl>
</td>
<td width="60%">
No container found.

</td>
</tr>
</table>

## -remarks

This function enumerates the cryptographic providers and their containers to find the private key that corresponds to the certificate's <a href="/windows/desktop/SecGloss/p-gly">public key</a>. For a match, the function updates the certificate's <b>CERT_KEY_PROV_INFO_PROP_ID</b> property. If the <b>CERT_KEY_PROV_INFO_PROP_ID</b> is already set, it is checked to determine whether it matches the provider's public key. For a match, the function skips the previously mentioned enumeration.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>