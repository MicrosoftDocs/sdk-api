---
UID: NF:bcrypt.BCryptImportKey
title: BCryptImportKey function (bcrypt.h)
description: Imports a symmetric key from a key BLOB.
helpviewer_keywords: ["BCRYPT_AES_WRAP_KEY_BLOB","BCRYPT_KEY_DATA_BLOB","BCRYPT_OPAQUE_KEY_BLOB","BCryptImportKey","BCryptImportKey function [Security]","bcrypt/BCryptImportKey","security.bcryptimportkey_func"]
old-location: security\bcryptimportkey_func.htm
tech.root: security
ms.assetid: 6b9683f4-10f2-40e4-9757-a1f01991bef7
ms.date: 12/05/2018
ms.keywords: BCRYPT_AES_WRAP_KEY_BLOB, BCRYPT_KEY_DATA_BLOB, BCRYPT_OPAQUE_KEY_BLOB, BCryptImportKey, BCryptImportKey function [Security], bcrypt/BCryptImportKey, security.bcryptimportkey_func
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
 - BCryptImportKey
 - bcrypt/BCryptImportKey
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
 - BCryptImportKey
---

# BCryptImportKey function


## -description

The <b>BCryptImportKey</b> function imports a symmetric key from a key <a href="/windows/desktop/SecGloss/b-gly">BLOB</a>. The <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptimportkeypair">BCryptImportKeyPair</a> function is used to import a <a href="/windows/desktop/SecGloss/p-gly">public/private key pair</a>.

## -parameters

### -param hAlgorithm [in]

The handle of the algorithm provider to import the key. This handle is obtained by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptopenalgorithmprovider">BCryptOpenAlgorithmProvider</a> function.

### -param hImportKey [in, optional]

The handle of the key encryption key needed to unwrap the key BLOB in the <i>pbInput</i> parameter.<div class="alert"><b>Note</b>  The handle must be supplied by the same provider that supplied the key that is being imported.</div>
<div> </div>


<b>Windows Server 2008 and Windows Vista:  </b>This parameter is not used and should be set to <b>NULL</b>.

### -param pszBlobType [in]

A null-terminated Unicode string that contains an identifier that specifies the type of BLOB that is contained in the <i>pbInput</i> buffer. This can be one of the following values.

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
Import a symmetric key from an AES key–wrapped key BLOB. The <i>hImportKey</i> parameter must reference a valid <b>BCRYPT_KEY_HANDLE</b> pointer to the key encryption key.

<b>Windows Server 2008 and Windows Vista:  </b>This BLOB type is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_KEY_DATA_BLOB"></a><a id="bcrypt_key_data_blob"></a><dl>
<dt><b>BCRYPT_KEY_DATA_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Import a symmetric key from a data BLOB. The <i>pbInput</i> parameter is a pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_key_data_blob_header">BCRYPT_KEY_DATA_BLOB_HEADER</a> structure immediately followed by the key BLOB.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_OPAQUE_KEY_BLOB"></a><a id="bcrypt_opaque_key_blob"></a><dl>
<dt><b>BCRYPT_OPAQUE_KEY_BLOB</b></dt>
</dl>
</td>
<td width="60%">
Import a symmetric key BLOB in a format that is specific to a single CSP. Opaque BLOBs are not transferable and must be imported by using the same CSP that generated the BLOB. Opaque BLOBs are only intended to be used for interprocess transfer of keys and are not suitable to be persisted and read in across versions of a provider.

</td>
</tr>
</table>

### -param phKey [out]

A pointer to a <b>BCRYPT_KEY_HANDLE</b> that receives the handle of the imported key. This handle is used in subsequent functions that require a key, such as <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a>. This handle must be released when it is no longer needed by passing it to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroykey">BCryptDestroyKey</a> function.

### -param pbKeyObject [out, optional]

A pointer to a buffer that receives the imported key object. The <i>cbKeyObject</i> parameter contains the size of this buffer. The required size of this buffer can be obtained by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgetproperty">BCryptGetProperty</a> function to get the <b>BCRYPT_OBJECT_LENGTH</b> property. This will provide the size of the key object for the specified algorithm.

This memory can only be freed after the <i>phKey</i> key handle is destroyed.

### -param cbKeyObject [in]

The size, in bytes, of the <i>pbKeyObject</i> buffer.

### -param pbInput [in]

The address of a buffer that contains the key BLOB to import. The <i>cbInput</i> parameter contains the size of this buffer. The <i>pszBlobType</i> parameter specifies the type of key BLOB this buffer contains.

### -param cbInput [in]

The size, in bytes, of the <i>pbInput</i> buffer.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are currently defined, so this parameter should be zero.

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
The size of the key object specified by the <i>cbKeyObject</i> parameter is not large enough to hold the key object.

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

When using a supported algorithm provider, <b>BCryptImportKey</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hAlgorithm</i> parameter must have been opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptImportKey</b> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroykey">BCryptDestroyKey</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptexportkey">BCryptExportKey</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptimportkeypair">BCryptImportKeyPair</a>