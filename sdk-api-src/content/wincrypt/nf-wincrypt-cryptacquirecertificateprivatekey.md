---
UID: NF:wincrypt.CryptAcquireCertificatePrivateKey
title: CryptAcquireCertificatePrivateKey function (wincrypt.h)
description: Obtains the private key for a certificate.
helpviewer_keywords: ["AT_KEYEXCHANGE","AT_SIGNATURE","CERT_NCRYPT_KEY_SPEC","CRYPT_ACQUIRE_WINDOW_HANDLE_FLAG","CRYPT_ACQUIRE_ALLOW_NCRYPT_KEY_FLAG","CRYPT_ACQUIRE_CACHE_FLAG","CRYPT_ACQUIRE_COMPARE_KEY_FLAG","CRYPT_ACQUIRE_NO_HEALING","CRYPT_ACQUIRE_ONLY_NCRYPT_KEY_FLAG","CRYPT_ACQUIRE_PREFER_NCRYPT_KEY_FLAG","CRYPT_ACQUIRE_SILENT_FLAG","CRYPT_ACQUIRE_USE_PROV_INFO_FLAG","CryptAcquireCertificatePrivateKey","CryptAcquireCertificatePrivateKey function [Security]","_crypto2_cryptacquirecertificateprivatekey","security.cryptacquirecertificateprivatekey","wincrypt/CryptAcquireCertificatePrivateKey"]
old-location: security\cryptacquirecertificateprivatekey.htm
tech.root: security
ms.assetid: 53c9aec9-701d-4c21-9814-d344a8dde0c1
ms.date: 12/05/2018
ms.keywords: AT_KEYEXCHANGE, AT_SIGNATURE, CERT_NCRYPT_KEY_SPEC, CRYPT_ACQUIRE_WINDOW_HANDLE_FLAG, CRYPT_ACQUIRE_ALLOW_NCRYPT_KEY_FLAG, CRYPT_ACQUIRE_CACHE_FLAG, CRYPT_ACQUIRE_COMPARE_KEY_FLAG, CRYPT_ACQUIRE_NO_HEALING, CRYPT_ACQUIRE_ONLY_NCRYPT_KEY_FLAG, CRYPT_ACQUIRE_PREFER_NCRYPT_KEY_FLAG, CRYPT_ACQUIRE_SILENT_FLAG, CRYPT_ACQUIRE_USE_PROV_INFO_FLAG, CryptAcquireCertificatePrivateKey, CryptAcquireCertificatePrivateKey function [Security], _crypto2_cryptacquirecertificateprivatekey, security.cryptacquirecertificateprivatekey, wincrypt/CryptAcquireCertificatePrivateKey
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
 - CryptAcquireCertificatePrivateKey
 - wincrypt/CryptAcquireCertificatePrivateKey
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
 - CryptAcquireCertificatePrivateKey
---

# CryptAcquireCertificatePrivateKey function


## -description

The <b>CryptAcquireCertificatePrivateKey</b> function obtains the <a href="/windows/desktop/SecGloss/p-gly">private key</a> for a certificate. This function is used to obtain access to a user's <a href="/windows/desktop/SecGloss/p-gly">private key</a> when the user's certificate is available, but the handle of the user's key container is not available. This function can only be used by the owner of a private key and not by any other user.

If a CSP handle and the key container containing a user's private key are available, the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetuserkey">CryptGetUserKey</a> function should be used instead.

## -parameters

### -param pCert [in]

The address of a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains the <a href="/windows/desktop/SecGloss/c-gly">certificate context</a> for which a private key will be obtained.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. This can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ACQUIRE_CACHE_FLAG"></a><a id="crypt_acquire_cache_flag"></a><dl>
<dt><b>CRYPT_ACQUIRE_CACHE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
If a handle is already acquired and cached, that same handle is returned. Otherwise, a new handle is acquired and cached by using the certificate's <b>CERT_KEY_CONTEXT_PROP_ID</b> property. 




When this flag is set, the <i>pfCallerFreeProvOrNCryptKey</i> parameter receives <b>FALSE</b> and the calling application must not release the handle. The handle is freed when the  certificate context is freed; however, you must retain the certificate context referenced by the <i>pCert</i> parameter as long as the key is in use, otherwise operations that rely on the key will fail.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ACQUIRE_COMPARE_KEY_FLAG"></a><a id="crypt_acquire_compare_key_flag"></a><dl>
<dt><b>CRYPT_ACQUIRE_COMPARE_KEY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/SecGloss/p-gly">public key</a> in the certificate is compared with the public key returned by the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP). If the keys do not match, the acquisition operation fails and the last error code is set to <b>NTE_BAD_PUBLIC_KEY</b>. If a cached handle is returned, no comparison is made.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ACQUIRE_NO_HEALING"></a><a id="crypt_acquire_no_healing"></a><dl>
<dt><b>CRYPT_ACQUIRE_NO_HEALING</b></dt>
</dl>
</td>
<td width="60%">
This function will not attempt to re-create the <b>CERT_KEY_PROV_INFO_PROP_ID</b> property in the certificate context if this property cannot be retrieved.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ACQUIRE_SILENT_FLAG"></a><a id="crypt_acquire_silent_flag"></a><dl>
<dt><b>CRYPT_ACQUIRE_SILENT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The CSP should not display any user interface (UI) for this context. If the CSP must display UI to operate, the call fails and the <b>NTE_SILENT_CONTEXT</b> error code is set as the last error.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ACQUIRE_USE_PROV_INFO_FLAG"></a><a id="crypt_acquire_use_prov_info_flag"></a><dl>
<dt><b>CRYPT_ACQUIRE_USE_PROV_INFO_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Uses the certificate's <b>CERT_KEY_PROV_INFO_PROP_ID</b> property to determine whether caching should be accomplished. For more information about the <b>CERT_KEY_PROV_INFO_PROP_ID</b> property, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>. 




This function will only use caching if during a previous call, the <i>dwFlags</i> member of the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a> structure contained <b>CERT_SET_KEY_CONTEXT_PROP</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ACQUIRE_WINDOW_HANDLE_FLAG"></a><a id="crypt_acquire_window_handle_flag"></a><dl>
<dt><b>CRYPT_ACQUIRE_WINDOW_HANDLE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Any UI that is needed by the CSP or KSP will be a child of the <b>HWND</b> that is supplied in the <i>pvParameters</i> parameter. For a CSP key, using this flag will cause the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetprovparam">CryptSetProvParam</a> function with the flag PP_CLIENT_HWND using this <b>HWND</b> to be called with <b>NULL</b> for <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a>.  For a KSP key, using this flag will cause the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptsetproperty">NCryptSetProperty</a> function with the NCRYPT_WINDOW_HANDLE_PROPERTY flag to be called using the <b>HWND</b>. 

Do not use this flag with <b>CRYPT_ACQUIRE_SILENT_FLAG</b>. 

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

The <i>pdwKeySpec</i> variable receives the <b>CERT_NCRYPT_KEY_SPEC</b> flag if CNG is used to obtain the key.

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

The <i>pdwKeySpec</i> variable receives the <b>CERT_NCRYPT_KEY_SPEC</b> flag if CNG is used to obtain the key.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ACQUIRE_PREFER_NCRYPT_KEY_FLAG"></a><a id="crypt_acquire_prefer_ncrypt_key_flag"></a><dl>
<dt><b>CRYPT_ACQUIRE_PREFER_NCRYPT_KEY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
This function will attempt to obtain the key by using CNG. If that fails, this function will attempt to obtain the key by using CryptoAPI. 

The <i>pdwKeySpec</i> variable receives the <b>CERT_NCRYPT_KEY_SPEC</b> flag if CNG is used to obtain the key.


<div class="alert"><b>Note</b>  CryptoAPI does not support the CNG Diffie-Hellman or DSA asymmetric algorithms. CryptoAPI only supports Diffie-Hellman and DSA public keys through the legacy CSPs. If this flag is set for a certificate that contains a Diffie-Hellman or DSA public key, this function will implicitly change this flag to <b>CRYPT_ACQUIRE_ALLOW_NCRYPT_KEY_FLAG</b> to first attempt to use CryptoAPI to obtain the key.</div>
<div> </div>


</td>
</tr>
</table>

### -param pvParameters [in, optional]

If the <b>CRYPT_ACQUIRE_WINDOW_HANDLE_FLAG</b>  is set, then this is the address of an <b>HWND</b>. If the <b>CRYPT_ACQUIRE_WINDOW_HANDLE_FLAG</b> is not set, then this parameter must be <b>NULL</b>.


<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This parameter was  named <i>pvReserved</i> and reserved for future use and must be <b>NULL</b>.

### -param phCryptProvOrNCryptKey [out]

The address of an <a href="/windows/desktop/SecCrypto/hcryptprov-or-ncrypt-key-handle">HCRYPTPROV_OR_NCRYPT_KEY_HANDLE</a> variable that receives the handle of either the CryptoAPI provider or the CNG key. If the <i>pdwKeySpec</i> variable receives the <b>CERT_NCRYPT_KEY_SPEC</b> flag, this is a CNG key handle of type <b>NCRYPT_KEY_HANDLE</b>; otherwise, this is a CryptoAPI provider handle of type <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a>.

For more information about when and how to release this handle, see the description of the <i>pfCallerFreeProvOrNCryptKey</i> parameter.

### -param pdwKeySpec [out]

The address of a <b>DWORD</b> variable that receives additional information about the key. This can be one of the following values.

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
The key pair is a key exchange pair.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_SIGNATURE"></a><a id="at_signature"></a><dl>
<dt><b>AT_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
The key pair is a signature pair.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NCRYPT_KEY_SPEC"></a><a id="cert_ncrypt_key_spec"></a><dl>
<dt><b>CERT_NCRYPT_KEY_SPEC</b></dt>
</dl>
</td>
<td width="60%">
The key is a CNG key.


<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.



</td>
</tr>
</table>

### -param pfCallerFreeProvOrNCryptKey [out]

The address of a <b>BOOL</b> variable that receives a value that indicates whether the caller must free the handle returned in the <i>phCryptProvOrNCryptKey</i> variable. This receives <b>FALSE</b> if any of the following is true:

<ul>
<li>Public key acquisition or comparison fails.</li>
<li>The <i>dwFlags</i> parameter contains the <b>CRYPT_ACQUIRE_CACHE_FLAG</b> flag.</li>
<li>The <i>dwFlags</i> parameter contains the <b>CRYPT_ACQUIRE_USE_PROV_INFO_FLAG</b> flag, the certificate context property is set to <b>CERT_KEY_PROV_INFO_PROP_ID</b> with the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a> structure, and the <i>dwFlags</i> member of the <b>CRYPT_KEY_PROV_INFO</b> structure is set to <b>CERT_SET_KEY_CONTEXT_PROP_ID</b>.</li>
</ul>
If this variable receives <b>FALSE</b>, the calling application must not release the handle returned in the <i>phCryptProvOrNCryptKey</i> variable. The handle will be released on the last free action of the <a href="/windows/desktop/SecGloss/c-gly">certificate context</a>.

If this variable receives <b>TRUE</b>, the caller is responsible for releasing the handle returned in the <i>phCryptProvOrNCryptKey</i> variable. If the <i>pdwKeySpec</i> variable receives the <b>CERT_NCRYPT_KEY_SPEC</b> value, the handle must be released by passing it to the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptfreeobject">NCryptFreeObject</a> function; otherwise, the handle is released by passing it to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptreleasecontext">CryptReleaseContext</a> function.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. One possible error code is the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_PUBLIC_KEY</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/SecGloss/p-gly">public key</a> in the <a href="/windows/desktop/SecGloss/c-gly">certificate</a> does not match the public key returned by the CSP. This error code is returned if the CRYPT_ACQUIRE_COMPARE_KEY_FLAG is set and the public key in the certificate does not match the public key returned by the cryptographic provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_SILENT_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter contained the <b>CRYPT_ACQUIRE_SILENT_FLAG</b> flag and the CSP could not continue an operation without displaying a user interface.

</td>
</tr>
</table>

## -remarks

When <b>CRYPT_ACQUIRE_WINDOW_HANDLE_FLAG</b> is set, the caller must ensure the <b>HWND</b> is valid. If the <b>HWND</b> is no longer valid, for CSP the caller should call <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetprovparam">CryptSetProvParam</a> using flag PP_CLIENT_HWND with <b>NULL</b> for the <b>HWND</b> and <b>NULL</b>  for the HCRYPTPROV. For KSP, the caller should set the  NCRYPT_WINDOW_HANDLE_PROPERTY of the ncrypt key to be <b>NULL</b>. When <b>CRYPT_ACQUIRE_WINDOW_HANDLE_FLAG</b> flag is set for KSP, the NCRYPT_WINDOW_HANDLE_PROPERTY is set on the storage provider and the key. If both calls fail, then the function fails. If only one fails, the function succeeds. Note that setting <b>HWND</b> to <b>NULL</b>  effectively removes <b>HWND</b> from the HCRYPTPROV or ncrypt key.


#### Examples

For an example that uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-sending-and-receiving-a-signed-and-encrypted-message">Example C Program: Sending and Receiving a Signed and Encrypted Message</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptreleasecontext">CryptReleaseContext</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Key Generation and Exchange Functions</a>
