---
UID: NF:bcrypt.BCryptImportKeyPair
title: BCryptImportKeyPair function (bcrypt.h)
description: Imports a public/private key pair from a key BLOB.
helpviewer_keywords: ["BCRYPT_DH_PRIVATE_BLOB","BCRYPT_DH_PUBLIC_BLOB","BCRYPT_DSA_PRIVATE_BLOB","BCRYPT_DSA_PUBLIC_BLOB","BCRYPT_ECCPRIVATE_BLOB","BCRYPT_ECCPUBLIC_BLOB","BCRYPT_NO_KEY_VALIDATION","BCRYPT_PRIVATE_KEY_BLOB","BCRYPT_PUBLIC_KEY_BLOB","BCRYPT_RSAPRIVATE_BLOB","BCRYPT_RSAPUBLIC_BLOB","BCryptImportKeyPair","BCryptImportKeyPair function [Security]","LEGACY_DH_PRIVATE_BLOB","LEGACY_DH_PUBLIC_BLOB","LEGACY_DSA_PRIVATE_BLOB","LEGACY_DSA_PUBLIC_BLOB","LEGACY_DSA_V2_PRIVATE_BLOB","LEGACY_RSAPRIVATE_BLOB","LEGACY_RSAPUBLIC_BLOB","bcrypt/BCryptImportKeyPair","security.bcryptimportkeypair"]
old-location: security\bcryptimportkeypair.htm
tech.root: security
ms.assetid: 271fc084-6121-4666-b521-b849c7d7966c
ms.date: 12/05/2018
ms.keywords: BCRYPT_DH_PRIVATE_BLOB, BCRYPT_DH_PUBLIC_BLOB, BCRYPT_DSA_PRIVATE_BLOB, BCRYPT_DSA_PUBLIC_BLOB, BCRYPT_ECCPRIVATE_BLOB, BCRYPT_ECCPUBLIC_BLOB, BCRYPT_NO_KEY_VALIDATION, BCRYPT_PRIVATE_KEY_BLOB, BCRYPT_PUBLIC_KEY_BLOB, BCRYPT_RSAPRIVATE_BLOB, BCRYPT_RSAPUBLIC_BLOB, BCryptImportKeyPair, BCryptImportKeyPair function [Security], LEGACY_DH_PRIVATE_BLOB, LEGACY_DH_PUBLIC_BLOB, LEGACY_DSA_PRIVATE_BLOB, LEGACY_DSA_PUBLIC_BLOB, LEGACY_DSA_V2_PRIVATE_BLOB, LEGACY_RSAPRIVATE_BLOB, LEGACY_RSAPUBLIC_BLOB, bcrypt/BCryptImportKeyPair, security.bcryptimportkeypair
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
 - BCryptImportKeyPair
 - bcrypt/BCryptImportKeyPair
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
 - BCryptImportKeyPair
---

# BCryptImportKeyPair function


## -description

The <b>BCryptImportKeyPair</b> function imports a <a href="/windows/win32/SecGloss/p-gly">public/private key pair</a> from a key <a href="/windows/win32/SecGloss/b-gly">BLOB</a>. The <a href="/windows/win32/api/bcrypt/nf-bcrypt-bcryptimportkey">BCryptImportKey</a> function is used to import a <a href="/windows/win32/SecGloss/s-gly">symmetric key</a>.

## -parameters

### -param hAlgorithm [in]

The handle of the algorithm provider to import the key. This handle is obtained by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptopenalgorithmprovider">BCryptOpenAlgorithmProvider</a> function.

### -param hImportKey [in, out]

This parameter is not currently used and should be <b>NULL</b>.

### -param pszBlobType [in]

A null-terminated Unicode string that contains an identifier that specifies the type of BLOB that is contained in the <i>pbInput</i> buffer. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DH_PRIVATE_BLOB"></a><a id="bcrypt_dh_private_blob"></a><dl>
<dt><b>BCRYPT_DH_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a Diffie-Hellman public/private key pair BLOB. The <i>pbInput</i> buffer must contain a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dh_key_blob">BCRYPT_DH_KEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DH_PUBLIC_BLOB"></a><a id="bcrypt_dh_public_blob"></a><dl>
<dt><b>BCRYPT_DH_PUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a Diffie-Hellman <a href="/windows/desktop/SecGloss/p-gly">public key BLOB</a>. The <i>pbInput</i> buffer must contain a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dh_key_blob">BCRYPT_DH_KEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DSA_PRIVATE_BLOB"></a><a id="bcrypt_dsa_private_blob"></a><dl>
<dt><b>BCRYPT_DSA_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a DSA public/private key pair BLOB. The <i>pbInput</i> buffer must contain a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dsa_key_blob">BCRYPT_DSA_KEY_BLOB</a> or <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dsa_key_blob_v2">BCRYPT_DSA_KEY_BLOB_V2</a> structure immediately followed by the key data. <b>BCRYPT_DSA_KEY_BLOB</b> is used for key lengths from 512 to 1024 bits. <b>BCRYPT_DSA_KEY_BLOB_V2</b> is used for key lengths that exceed 1024 bits but are less than or equal to 3072 bits.

<b>Windows 8:  </b>Support for <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dsa_key_blob_v2">BCRYPT_DSA_KEY_BLOB_V2</a> begins.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_DSA_PUBLIC_BLOB"></a><a id="bcrypt_dsa_public_blob"></a><dl>
<dt><b>BCRYPT_DSA_PUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a DSA public key BLOB. The <i>pbInput</i> buffer must contain a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dsa_key_blob">BCRYPT_DSA_KEY_BLOB</a> or <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dsa_key_blob_v2">BCRYPT_DSA_KEY_BLOB_V2</a> structure immediately followed by the key data. <b>BCRYPT_DSA_KEY_BLOB</b> is used for key lengths from 512 to 1024 bits. <b>BCRYPT_DSA_KEY_BLOB_V2</b> is used for key lengths that exceed 1024 bits but are less than or equal to 3072 bits.

<b>Windows 8:  </b>Support for <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dsa_key_blob_v2">BCRYPT_DSA_KEY_BLOB_V2</a> begins.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ECCPRIVATE_BLOB"></a><a id="bcrypt_eccprivate_blob"></a><dl>
<dt><b>BCRYPT_ECCPRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an <a href="/windows/desktop/SecGloss/e-gly">elliptic curve cryptography</a> (ECC) <a href="/windows/desktop/SecGloss/p-gly">private key</a>. The <i>pbInput</i> buffer must contain a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_ecckey_blob">BCRYPT_ECCKEY_BLOB</a> structure immediately followed by the key data. 

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ECCPUBLIC_BLOB"></a><a id="bcrypt_eccpublic_blob"></a><dl>
<dt><b>BCRYPT_ECCPUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an ECC public key. The <i>pbInput</i> buffer must contain a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_ecckey_blob">BCRYPT_ECCKEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PUBLIC_KEY_BLOB"></a><a id="bcrypt_public_key_blob"></a><dl>
<dt><b>BCRYPT_PUBLIC_KEY_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a generic <a href="/windows/desktop/SecGloss/p-gly">public key</a> of any type. The type of key in this BLOB is determined by the <b>Magic</b> member of the <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_key_blob">BCRYPT_KEY_BLOB</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PRIVATE_KEY_BLOB"></a><a id="bcrypt_private_key_blob"></a><dl>
<dt><b>BCRYPT_PRIVATE_KEY_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a generic private key of any type. The private key does not necessarily contain the public key. The type of key in this BLOB is determined by the <b>Magic</b> member of the <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_key_blob">BCRYPT_KEY_BLOB</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RSAPRIVATE_BLOB"></a><a id="bcrypt_rsaprivate_blob"></a><dl>
<dt><b>BCRYPT_RSAPRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an RSA public/private key pair BLOB. The <i>pbInput</i> buffer must contain a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_rsakey_blob">BCRYPT_RSAKEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RSAPUBLIC_BLOB"></a><a id="bcrypt_rsapublic_blob"></a><dl>
<dt><b>BCRYPT_RSAPUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an RSA public key BLOB. The <i>pbInput</i> buffer must contain a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_rsakey_blob">BCRYPT_RSAKEY_BLOB</a> structure immediately followed by the key data.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DH_PUBLIC_BLOB"></a><a id="legacy_dh_public_blob"></a><dl>
<dt><b>LEGACY_DH_PUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a Diffie-Hellman public key BLOB that was exported by using <a href="/windows/desktop/SecGloss/c-gly">CryptoAPI</a>. The Microsoft primitive provider does not support importing this BLOB type.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DH_PRIVATE_BLOB"></a><a id="legacy_dh_private_blob"></a><dl>
<dt><b>LEGACY_DH_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a legacy <a href="/windows/desktop/SecCrypto/diffie-hellman-version-3-private-key-blobs">Diffie-Hellman Version 3 Private Key BLOB</a> that contains a Diffie-Hellman public/private key pair that was exported by using CryptoAPI.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DSA_PRIVATE_BLOB"></a><a id="legacy_dsa_private_blob"></a><dl>
<dt><b>LEGACY_DSA_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a DSA public/private key pair BLOB that was exported by using CryptoAPI.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DSA_PUBLIC_BLOB"></a><a id="legacy_dsa_public_blob"></a><dl>
<dt><b>LEGACY_DSA_PUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a DSA public key BLOB that was exported by using CryptoAPI. The Microsoft primitive provider does not support importing this BLOB type.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_DSA_V2_PRIVATE_BLOB"></a><a id="legacy_dsa_v2_private_blob"></a><dl>
<dt><b>LEGACY_DSA_V2_PRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is a DSA version 2 private key in a form that can be imported by using CryptoAPI.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_RSAPRIVATE_BLOB"></a><a id="legacy_rsaprivate_blob"></a><dl>
<dt><b>LEGACY_RSAPRIVATE_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an RSA public/private key pair BLOB that was exported by using CryptoAPI.

</td>
</tr>
<tr>
<td width="40%"><a id="LEGACY_RSAPUBLIC_BLOB"></a><a id="legacy_rsapublic_blob"></a><dl>
<dt><b>LEGACY_RSAPUBLIC_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The BLOB is an RSA public key BLOB that was exported by using CryptoAPI. The Microsoft primitive provider does not support importing this BLOB type.

</td>
</tr>
</table>

### -param phKey [out]

A pointer to a <b>BCRYPT_KEY_HANDLE</b> that receives the handle of the imported key. This handle is used in subsequent functions that require a key, such as <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsignhash">BCryptSignHash</a>. This handle must be released when it is no longer needed by passing it to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroykey">BCryptDestroyKey</a> function.

### -param pbInput [in]

The address of a buffer that contains the <a href="/windows/desktop/SecGloss/k-gly">key BLOB</a> to import. The <i>cbInput</i> parameter contains the size of this buffer. The <i>pszBlobType</i> parameter specifies the type of key BLOB this buffer contains.

### -param cbInput [in]

The size, in bytes, of the <i>pbInput</i> buffer.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. This can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_NO_KEY_VALIDATION"></a><a id="bcrypt_no_key_validation"></a><dl>
<dt><b>BCRYPT_NO_KEY_VALIDATION</b></dt>
</dl>
</td>
<td width="60%">
Do not validate the public portion of the key pair.

</td>
</tr>
</table>

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
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The algorithm handle in the <i>hAlgorithm</i> parameter is not valid.

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
The algorithm provider specified by the <i>hAlgorithm</i> parameter does not support the BLOB type specified by the <i>pszBlobType</i> parameter.

</td>
</tr>
</table>

## -remarks

Depending on what processor modes a provider supports, <b>BCryptImportKeyPair</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hAlgorithm</i> parameter must have been opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptImportKeyPair</b> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroykey">BCryptDestroyKey</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptexportkey">BCryptExportKey</a>



<a href="/windows/win32/api/bcrypt/nf-bcrypt-bcryptimportkey">BCryptImportKey</a>
