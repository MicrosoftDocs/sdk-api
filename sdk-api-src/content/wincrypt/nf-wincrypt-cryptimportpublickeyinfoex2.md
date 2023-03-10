---
UID: NF:wincrypt.CryptImportPublicKeyInfoEx2
title: CryptImportPublicKeyInfoEx2 function (wincrypt.h)
description: Imports a public key into the CNG asymmetric provider that corresponds to the public key object identifier (OID) and returns a CNG handle to the key.
helpviewer_keywords: ["CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG","CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG","CryptImportPublicKeyInfoEx2","CryptImportPublicKeyInfoEx2 function [Security]","X509_ASN_ENCODING","security.cryptimportpublickeyinfoex2","wincrypt/CryptImportPublicKeyInfoEx2"]
old-location: security\cryptimportpublickeyinfoex2.htm
tech.root: security
ms.assetid: c73f2499-75e9-4146-ae4c-0e949206ea37
ms.date: 12/05/2018
ms.keywords: CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG, CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG, CryptImportPublicKeyInfoEx2, CryptImportPublicKeyInfoEx2 function [Security], X509_ASN_ENCODING, security.cryptimportpublickeyinfoex2, wincrypt/CryptImportPublicKeyInfoEx2
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - CryptImportPublicKeyInfoEx2
 - wincrypt/CryptImportPublicKeyInfoEx2
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
 - CryptImportPublicKeyInfoEx2
---

# CryptImportPublicKeyInfoEx2 function


## -description

The <b>CryptImportPublicKeyInfoEx2</b> function imports a public key into the CNG asymmetric provider that corresponds to the <a href="/windows/desktop/SecGloss/p-gly">public key</a> <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and returns a CNG handle to the key.

## -parameters

### -param dwCertEncodingType [in]

The <a href="/windows/desktop/SecGloss/c-gly">certificate encoding type</a> that was used to encrypt the subject. The <a href="/windows/desktop/SecGloss/m-gly">message encoding type</a> identifier, contained in the high <b>WORD</b> of this value, is ignored by this function.


This parameter can be the following currently defined certificate encoding type.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="X509_ASN_ENCODING"></a><a id="x509_asn_encoding"></a><dl>
<dt><b>X509_ASN_ENCODING</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Specifies <a href="/windows/desktop/SecGloss/x-gly">X.509</a> certificate encoding.

</td>
</tr>
</table>

### -param pInfo [in]

The address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure that contains the public key information to import into the provider.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. This can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG"></a><a id="crypt_oid_info_pubkey_sign_key_flag"></a><dl>
<dt><b>CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Skips public keys in the CRYPT_PUBKEY_ALG_OID_GROUP_ID group that are explicitly flagged with the CRYPT_OID_PUBKEY_ENCRYPT_ONLY_FLAG flag.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG"></a><a id="crypt_oid_info_pubkey_encrypt_key_flag"></a><dl>
<dt><b>CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Skips public keys in the CRYPT_PUBKEY_ALG_OID_GROUP_ID group that are explicitly flagged with the CRYPT_OID_PUBKEY_SIGN_ONLY_FLAG flag.

</td>
</tr>
</table>
 

These flags are passed in the <i>dwKeyType</i> parameter of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo">CryptFindOIDInfo</a> function when mapping the public key object identifier to the corresponding CNG public key algorithm identifier.

### -param pvAuxInfo [in]

This parameter is reserved for future use and must be set to <b>NULL</b>.

### -param phKey [out]

The address of a <b>BCRYPT_KEY_HANDLE</b> variable that receives the handle of the imported key.

When this handle is no longer needed, you must release it by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroykey">BCryptDestroyKey</a> function.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error codes include, but are not limited to, the following.

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
An import function that can be installed or registered could not be found for the specified <i>dwCertEncodingType</i> and <i>pInfo</i> parameters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a>