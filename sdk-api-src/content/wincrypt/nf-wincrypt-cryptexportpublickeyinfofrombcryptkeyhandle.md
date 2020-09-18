---
UID: NF:wincrypt.CryptExportPublicKeyInfoFromBCryptKeyHandle
title: CryptExportPublicKeyInfoFromBCryptKeyHandle function (wincrypt.h)
description: Exports the public key information associated with a provider's corresponding private key.
helpviewer_keywords: ["CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG","CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG","CryptExportPublicKeyInfoFromBCryptKeyHandle","CryptExportPublicKeyInfoFromBCryptKeyHandle function [Security]","security.cryptexportpublickeyinfofrombcryptkeyhandle","wincrypt/CryptExportPublicKeyInfoFromBCryptKeyHandle"]
old-location: security\cryptexportpublickeyinfofrombcryptkeyhandle.htm
tech.root: security
ms.assetid: f96bff4a-d354-4231-907a-383aff5cfacc
ms.date: 12/05/2018
ms.keywords: CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG, CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG, CryptExportPublicKeyInfoFromBCryptKeyHandle, CryptExportPublicKeyInfoFromBCryptKeyHandle function [Security], security.cryptexportpublickeyinfofrombcryptkeyhandle, wincrypt/CryptExportPublicKeyInfoFromBCryptKeyHandle
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - CryptExportPublicKeyInfoFromBCryptKeyHandle
 - wincrypt/CryptExportPublicKeyInfoFromBCryptKeyHandle
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
 - CryptExportPublicKeyInfoFromBCryptKeyHandle
---

# CryptExportPublicKeyInfoFromBCryptKeyHandle function


## -description

The <b>CryptExportPublicKeyInfoFromBCryptKeyHandle</b> function exports the <a href="/windows/desktop/SecGloss/p-gly">public key</a> information associated with a provider's corresponding  <a href="/windows/desktop/SecGloss/p-gly">private key</a>.

## -parameters

### -param hBCryptKey [in]

The handle of the key from which to export the public key information.

### -param dwCertEncodingType [in]

Specifies the encoding type to be matched.  



						

This value can be a bitwise combination of the currently defined encoding types:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pszPublicKeyObjId [in, optional]

A pointer to the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) that identifies the installable function to  use to export the key. If the high-order word of the OID is nonzero, <i>pszPublicKeyObjId</i> is a pointer to either an OID string such as "2.5.29.1" or an ASCII string such as "file." If the high-order word of the OID is zero, the low-order word specifies the integer identifier to be used as the object identifier.

### -param dwFlags [in]

A <b>DWORD</b> value that indicates how the public key information  is exported.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG"></a><a id="crypt_oid_info_pubkey_sign_key_flag"></a><dl>
<dt><b>CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Skips public keys in the <b>CRYPT_PUBKEY_ALG_OID_GROUP_ID</b> group that are explicitly flagged with the <b>CRYPT_OID_PUBKEY_ENCRYPT_ONLY_FLAG</b> flag.


</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG"></a><a id="crypt_oid_info_pubkey_encrypt_key_flag"></a><dl>
<dt><b>CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
Skips public keys in the <b>CRYPT_PUBKEY_ALG_OID_GROUP_ID</b> group that are explicitly flagged with the <b>CRYPT_OID_PUBKEY_SIGN_ONLY_FLAG</b> flag.


</td>
</tr>
</table>

### -param pvAuxInfo [in, optional]

This parameter is reserved for future use and  must be set to <b>NULL</b>.

### -param pInfo [out, optional]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a>  structure to receive the public key information to be exported.

This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbInfo [in, out]

A pointer to a <b>DWORD</b> that contains the size, in bytes, of the buffer pointed to by the <i>pInfo</i> parameter. When the function returns, the <b>DWORD</b> contains the number of bytes stored in the buffer.

## -returns

The function returns <b>TRUE</b> if it succeeds; otherwise, it returns <b>FALSE</b>.

## -remarks

  If the <b>CryptExportPublicKeyInfoFromBCryptKeyHandle</b> function is unable to find an installable OID function for the OID specified by the <i>pszPublicKeyObjId</i> parameter, it attempts to export the key as a RSA Public Key (<b>szOID_RSA_RSA</b>).
 If the key is exported as a RSA Public Key, the values of the <i>dwFlags</i> and <i>pvAuxInfo</i> parameters are not used.