---
UID: NF:ncrypt.NCryptCreatePersistedKey
title: NCryptCreatePersistedKey function (ncrypt.h)
description: Creates a new key and stores it in the specified key storage provider.
helpviewer_keywords: ["AT_KEYEXCHANGE","AT_SIGNATURE","NCRYPT_MACHINE_KEY_FLAG","NCRYPT_OVERWRITE_KEY_FLAG","NCryptCreatePersistedKey","NCryptCreatePersistedKey function [Security]","ncrypt/NCryptCreatePersistedKey","security.ncryptcreatepersistedkey_func"]
old-location: security\ncryptcreatepersistedkey_func.htm
tech.root: security
ms.assetid: eeb1842f-fd9e-4edf-9db8-7b4e91760e9b
ms.date: 12/05/2018
ms.keywords: AT_KEYEXCHANGE, AT_SIGNATURE, NCRYPT_MACHINE_KEY_FLAG, NCRYPT_OVERWRITE_KEY_FLAG, NCryptCreatePersistedKey, NCryptCreatePersistedKey function [Security], ncrypt/NCryptCreatePersistedKey, security.ncryptcreatepersistedkey_func
req.header: ncrypt.h
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
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptCreatePersistedKey
 - ncrypt/NCryptCreatePersistedKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ncrypt.dll
api_name:
 - NCryptCreatePersistedKey
---

# NCryptCreatePersistedKey function


## -description

The <b>NCryptCreatePersistedKey</b> function creates a new key and stores it in the specified key storage provider. After you create a key by using this function, you can use the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptsetproperty">NCryptSetProperty</a> function to set its properties; however, the key cannot be used until the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptfinalizekey">NCryptFinalizeKey</a> function is called.

## -parameters

### -param hProvider [in]

The handle of the key storage provider to create the key in. This handle is obtained by using the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptopenstorageprovider">NCryptOpenStorageProvider</a> function.

### -param phKey [out]

The address of an <b>NCRYPT_KEY_HANDLE</b> variable that receives the handle of the key. When you have finished using this handle, release it by passing it to the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptfreeobject">NCryptFreeObject</a> function. To delete the key file on disk, pass the handle to the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptdeletekey">NCryptDeleteKey</a> function. This will also release the handle. So applications may pass the handle to either <b>NCryptFreeObject</b> or <b>NCryptDeleteKey</b>, but not both. 

### -param pszAlgId [in]

A pointer to a null-terminated Unicode string that contains the identifier of the cryptographic algorithm to create the key. This can be one of the standard <a href="/windows/desktop/SecCNG/cng-algorithm-identifiers">CNG Algorithm Identifiers</a> or the identifier for another registered algorithm.

### -param pszKeyName [in, optional]

A pointer to a null-terminated Unicode string that contains the name of the key. If this parameter is <b>NULL</b>, this function will create an ephemeral key that is not persisted.

### -param dwLegacyKeySpec [in]

A legacy identifier that specifies the type of key. This can be one of the following values.

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
The key is a key exchange key.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_SIGNATURE"></a><a id="at_signature"></a><dl>
<dt><b>AT_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
The key is a signature key.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The key is none of the above types.

</td>
</tr>
</table>

### -param dwFlags [in]

A set of flags that modify the behavior of this function. This can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_MACHINE_KEY_FLAG"></a><a id="ncrypt_machine_key_flag"></a><dl>
<dt><b>NCRYPT_MACHINE_KEY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The key applies to the local computer. If this flag is not present, the key applies to the current user.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_OVERWRITE_KEY_FLAG"></a><a id="ncrypt_overwrite_key_flag"></a><dl>
<dt><b>NCRYPT_OVERWRITE_KEY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
If a key already exists in the container with the specified name, the existing key will be overwritten. If this flag is not specified and a key with the specified name already exists, this function will return <b>NTE_EXISTS</b>.

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
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter contains a value that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
A key with the specified name already exists and the <b>NCRYPT_OVERWRITE_KEY_FLAG</b> was not specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hProvider</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -remarks

If you are creating an RSA key pair, you can also have the key stored in legacy storage so that it can be used with the CryptoAPI by passing the <b>NCRYPT_WRITE_KEY_TO_LEGACY_STORE_FLAG</b> flag to the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptfinalizekey">NCryptFinalizeKey</a> function when the key is finalized.

A service must not call this function from its <a href="/windows/win32/api/winsvc/nf-winsvc-startservicea">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.

## -see-also

<a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptdeletekey">NCryptDeleteKey</a>



<a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptfinalizekey">NCryptFinalizeKey</a>
