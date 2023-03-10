---
UID: NF:bcrypt.BCryptExportKey
title: BCryptExportKey function (bcrypt.h)
description: Exports a key to a memory BLOB that can be persisted for later use.
helpviewer_keywords: ["BCRYPT_AES_WRAP_KEY_BLOB","BCRYPT_DH_PRIVATE_BLOB","BCRYPT_DH_PUBLIC_BLOB","BCRYPT_DSA_PRIVATE_BLOB","BCRYPT_DSA_PUBLIC_BLOB","BCRYPT_ECCPRIVATE_BLOB","BCRYPT_ECCPUBLIC_BLOB","BCRYPT_KEY_DATA_BLOB","BCRYPT_OPAQUE_KEY_BLOB","BCRYPT_PRIVATE_KEY_BLOB","BCRYPT_PUBLIC_KEY_BLOB","BCRYPT_RSAFULLPRIVATE_BLOB","BCRYPT_RSAPRIVATE_BLOB","BCRYPT_RSAPUBLIC_BLOB","BCryptExportKey","BCryptExportKey function [Security]","LEGACY_DH_PRIVATE_BLOB","LEGACY_DH_PUBLIC_BLOB","LEGACY_DSA_PRIVATE_BLOB","LEGACY_DSA_PUBLIC_BLOB","LEGACY_DSA_V2_PRIVATE_BLOB","LEGACY_RSAPRIVATE_BLOB","LEGACY_RSAPUBLIC_BLOB","bcrypt/BCryptExportKey","security.bcryptexportkey_func"]
old-location: security\bcryptexportkey_func.htm
tech.root: security
ms.assetid: a5d73143-c1d6-43b3-a724-7e27c68a5ade
ms.date: 12/05/2018
ms.keywords: BCRYPT_AES_WRAP_KEY_BLOB, BCRYPT_DH_PRIVATE_BLOB, BCRYPT_DH_PUBLIC_BLOB, BCRYPT_DSA_PRIVATE_BLOB, BCRYPT_DSA_PUBLIC_BLOB, BCRYPT_ECCPRIVATE_BLOB, BCRYPT_ECCPUBLIC_BLOB, BCRYPT_KEY_DATA_BLOB, BCRYPT_OPAQUE_KEY_BLOB, BCRYPT_PRIVATE_KEY_BLOB, BCRYPT_PUBLIC_KEY_BLOB, BCRYPT_RSAFULLPRIVATE_BLOB, BCRYPT_RSAPRIVATE_BLOB, BCRYPT_RSAPUBLIC_BLOB, BCryptExportKey, BCryptExportKey function [Security], LEGACY_DH_PRIVATE_BLOB, LEGACY_DH_PUBLIC_BLOB, LEGACY_DSA_PRIVATE_BLOB, LEGACY_DSA_PUBLIC_BLOB, LEGACY_DSA_V2_PRIVATE_BLOB, LEGACY_RSAPRIVATE_BLOB, LEGACY_RSAPUBLIC_BLOB, bcrypt/BCryptExportKey, security.bcryptexportkey_func
req.header: bcrypt.h
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
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCryptExportKey
 - bcrypt/BCryptExportKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
 - Ksecdd.sys
api_name:
 - BCryptExportKey
---

# BCryptExportKey function


## -description

The <b>BCryptExportKey</b> function exports a key to a memory <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> that can be persisted for later use.

## -parameters

### -param hKey [in]

The handle of the key to export.

### -param hExportKey [in]

The handle of the key with which to wrap the exported key. Use this parameter when exporting BLOBs of type <b>BCRYPT_AES_WRAP_KEY_BLOB</b>; otherwise, set it to <b>NULL</b>.<div class="alert"><b>Note</b>  The <i>hExportKey</i> handle must be supplied by the same provider that supplied the <i>hKey</i> handle, and <i>hExportKey</i> must be a handle to a symmetric key that can be used in the <a href="/windows/desktop/SecGloss/a-gly">Advanced Encryption Standard</a> (AES) key wrap algorithm. When the <i>hKey</i> handle is from the Microsoft provider, <i>hExportKey</i> must be an AES key handle.</div>
<div> </div>


<b>Windows Server 2008 and Windows Vista:  </b>This parameter is not used and should be set to <b>NULL</b>.

### -param pszBlobType [in]

A null-terminated Unicode string that contains an identifier that specifies the type of BLOB to export. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_AES_WRAP_KEY_BLOB"></a><a id="bcrypt_aes_wrap_key_blob"></a><dl>
<dt><b>BCRYPT_AES_WRAP_KEY_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export  an AES key wrapped key. The <i>hExportKey</i> parameter must reference a valid <b>BCRYPT_KEY_HANDLE</b> pointer to the key encryption key, and the key represented by the <i>hKey</i> parameter must be a multiple of 8 bytes long.

<b>Windows Server 2008 and Windows Vista:  </b>This BLOB type is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DH_PRIVATE_BLOB"></a><a id="bcrypt_dh_private_blob"></a><dl>
<dt><b>BCRYPT_DH_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export a Diffie-Hellman <a href="/windows/desktop/SecGloss/p-gly">public/private key pair</a>. The <i>pbOutput</i> buffer receives a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dh_key_blob">BCRYPT_DH_KEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DH_PUBLIC_BLOB"></a><a id="bcrypt_dh_public_blob"></a><dl>
<dt><b>BCRYPT_DH_PUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export a Diffie-Hellman <a href="/windows/desktop/SecGloss/p-gly">public key</a>. The <i>pbOutput</i> buffer receives a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dh_key_blob">BCRYPT_DH_KEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DSA_PRIVATE_BLOB"></a><a id="bcrypt_dsa_private_blob"></a><dl>
<dt><b>BCRYPT_DSA_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export a DSA public/private key pair. The <i>pbOutput</i> buffer receives a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dsa_key_blob">BCRYPT_DSA_KEY_BLOB</a> or <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dsa_key_blob_v2">BCRYPT_DSA_KEY_BLOB_V2</a> structure immediately followed by the key data. <b>BCRYPT_DSA_KEY_BLOB</b> is used for key lengths from 512 to 1024 bits. <b>BCRYPT_DSA_KEY_BLOB_V2</b> is used for key lengths that exceed 1024 bits but are less than or equal to 3072 bits.

<b>Windows 8:  </b>Support for <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dsa_key_blob_v2">BCRYPT_DSA_KEY_BLOB_V2</a> begins.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DSA_PUBLIC_BLOB"></a><a id="bcrypt_dsa_public_blob"></a><dl>
<dt><b>BCRYPT_DSA_PUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export a DSA public key. The <i>pbOutput</i> buffer receives a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dsa_key_blob">BCRYPT_DSA_KEY_BLOB</a> or <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dsa_key_blob_v2">BCRYPT_DSA_KEY_BLOB_V2</a> structure immediately followed by the key data.  <b>BCRYPT_DSA_KEY_BLOB</b> is used for key lengths from 512 to 1024 bits. <b>BCRYPT_DSA_KEY_BLOB_V2</b> is used for key lengths that exceed 1024 bits but are less than or equal to 3072 bits.

<b>Windows 8:  </b>Support for <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dsa_key_blob_v2">BCRYPT_DSA_KEY_BLOB_V2</a> begins.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ECCPRIVATE_BLOB"></a><a id="bcrypt_eccprivate_blob"></a><dl>
<dt><b>BCRYPT_ECCPRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export an <a href="/windows/desktop/SecGloss/e-gly">elliptic curve cryptography</a> (ECC) <a href="/windows/desktop/SecGloss/p-gly">private key</a>. The <i>pbOutput</i> buffer receives a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_ecckey_blob">BCRYPT_ECCKEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ECCPUBLIC_BLOB"></a><a id="bcrypt_eccpublic_blob"></a><dl>
<dt><b>BCRYPT_ECCPUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export an ECC public key. The <i>pbOutput</i> buffer receives a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_ecckey_blob">BCRYPT_ECCKEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_KEY_DATA_BLOB"></a><a id="bcrypt_key_data_blob"></a><dl>
<dt><b>BCRYPT_KEY_DATA_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export a symmetric key to a data BLOB. The <i>pbOutput</i> buffer receives a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_key_data_blob_header">BCRYPT_KEY_DATA_BLOB_HEADER</a> structure immediately followed by the key BLOB.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_OPAQUE_KEY_BLOB"></a><a id="bcrypt_opaque_key_blob"></a><dl>
<dt><b>BCRYPT_OPAQUE_KEY_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export a symmetric key in a format that is specific to a single <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP). Opaque BLOBs are not transferable and must be imported by using the same CSP that generated the BLOB. Opaque BLOBs are only intended to be used for interprocess transfer of keys and are not suitable to be persisted and read across versions of a provider.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PUBLIC_KEY_BLOB"></a><a id="bcrypt_public_key_blob"></a><dl>
<dt><b>BCRYPT_PUBLIC_KEY_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export a generic public key of any type. The type of key in this BLOB is determined by the <b>Magic</b> member of the <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_key_blob">BCRYPT_KEY_BLOB</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PRIVATE_KEY_BLOB"></a><a id="bcrypt_private_key_blob"></a><dl>
<dt><b>BCRYPT_PRIVATE_KEY_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export a generic private key of any type. The private key does not necessarily contain the public key. The type of key in this BLOB is determined by the <b>Magic</b> member of the <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_key_blob">BCRYPT_KEY_BLOB</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RSAFULLPRIVATE_BLOB"></a><a id="bcrypt_rsafullprivate_blob"></a><dl>
<dt><b>BCRYPT_RSAFULLPRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export a full RSA public/private key pair. The <i>pbOutput</i> buffer receives a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_rsakey_blob">BCRYPT_RSAKEY_BLOB</a> structure immediately followed by the key data. This BLOB will include additional key material compared to the <b>BCRYPT_RSAPRIVATE_BLOB</b> type.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RSAPRIVATE_BLOB"></a><a id="bcrypt_rsaprivate_blob"></a><dl>
<dt><b>BCRYPT_RSAPRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export an RSA public/private key pair. The <i>pbOutput</i> buffer receives a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_rsakey_blob">BCRYPT_RSAKEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RSAPUBLIC_BLOB"></a><a id="bcrypt_rsapublic_blob"></a><dl>
<dt><b>BCRYPT_RSAPUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export an RSA public key. The <i>pbOutput</i> buffer receives a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_rsakey_blob">BCRYPT_RSAKEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DH_PRIVATE_BLOB"></a><a id="legacy_dh_private_blob"></a><dl>
<dt><b>LEGACY_DH_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export a legacy <a href="/windows/desktop/SecCrypto/diffie-hellman-version-3-private-key-blobs">Diffie-Hellman Version 3 Private Key BLOB</a> that contains a Diffie-Hellman public/private key pair that can be imported by using <a href="/windows/desktop/SecGloss/c-gly">CryptoAPI</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DH_PUBLIC_BLOB"></a><a id="legacy_dh_public_blob"></a><dl>
<dt><b>LEGACY_DH_PUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export a legacy <a href="/windows/desktop/SecCrypto/diffie-hellman-version-3-public-key-blobs">Diffie-Hellman Version 3 Public Key BLOB</a> that contains a Diffie-Hellman public key that can be imported by using CryptoAPI.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DSA_PRIVATE_BLOB"></a><a id="legacy_dsa_private_blob"></a><dl>
<dt><b>LEGACY_DSA_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export a DSA public/private key pair in a form that can be imported by using CryptoAPI.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DSA_PUBLIC_BLOB"></a><a id="legacy_dsa_public_blob"></a><dl>
<dt><b>LEGACY_DSA_PUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export a DSA public key in a form that can be imported by using CryptoAPI.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DSA_V2_PRIVATE_BLOB"></a><a id="legacy_dsa_v2_private_blob"></a><dl>
<dt><b>LEGACY_DSA_V2_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export a DSA version 2 private key in a form that can be imported by using CryptoAPI.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_RSAPRIVATE_BLOB"></a><a id="legacy_rsaprivate_blob"></a><dl>
<dt><b>LEGACY_RSAPRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export an RSA public/private key pair in a form that can be imported by using CryptoAPI.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_RSAPUBLIC_BLOB"></a><a id="legacy_rsapublic_blob"></a><dl>
<dt><b>LEGACY_RSAPUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Export an RSA public key in a form that can be imported by using CryptoAPI.

</td>
</tr>
</table>

### -param pbOutput [out]

The address of a buffer that receives the key BLOB. The <i>cbOutput</i> parameter contains the size of this buffer. If this parameter is <b>NULL</b>, this function will place the required size, in bytes, in the <b>ULONG</b> pointed to by the <i>pcbResult</i> parameter.

### -param cbOutput [in]

Contains the size, in bytes, of the <i>pbOutput</i> buffer.

### -param pcbResult [out]

A pointer to a <b>ULONG</b> that receives the number of bytes that were copied to the <i>pbOutput</i> buffer. If the <i>pbOutput</i> parameter is <b>NULL</b>, this function will place the required size, in bytes, in the <b>ULONG</b> pointed to by this parameter.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are defined for this function.

## -returns

Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The size specified by the <i>cbOutput</i> parameter is not large enough to hold the ciphertext.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The key handle in the <i>hKey</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The specified BLOB type is not supported by the provider.

</td>
</tr>
</table>

## -remarks

Depending on what processor modes a provider supports, <b>BCryptExportKey</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hKey</i> parameter must be derived from an algorithm handle returned by a provider that was opened with the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptExportKey</b> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptimportkey">BCryptImportKey</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptimportkeypair">BCryptImportKeyPair</a>