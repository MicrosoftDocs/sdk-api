---
UID: NF:bcrypt.BCryptQueryContextFunctionProperty
title: BCryptQueryContextFunctionProperty function (bcrypt.h)
description: Obtains the value of a named property for a cryptographic function in an existing CNG context.
helpviewer_keywords: ["BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE","BCRYPT_CIPHER_INTERFACE","BCRYPT_HASH_INTERFACE","BCRYPT_RNG_INTERFACE","BCRYPT_SECRET_AGREEMENT_INTERFACE","BCRYPT_SIGNATURE_INTERFACE","BCryptQueryContextFunctionProperty","BCryptQueryContextFunctionProperty function [Security]","CRYPT_DOMAIN","CRYPT_LOCAL","NCRYPT_KEY_STORAGE_INTERFACE","NCRYPT_SCHANNEL_INTERFACE","bcrypt/BCryptQueryContextFunctionProperty","security.bcryptquerycontextfunctionproperty"]
old-location: security\bcryptquerycontextfunctionproperty.htm
tech.root: security
ms.assetid: c8814a13-ac28-4583-927f-c787e0a25faf
ms.date: 12/05/2018
ms.keywords: BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE, BCRYPT_CIPHER_INTERFACE, BCRYPT_HASH_INTERFACE, BCRYPT_RNG_INTERFACE, BCRYPT_SECRET_AGREEMENT_INTERFACE, BCRYPT_SIGNATURE_INTERFACE, BCryptQueryContextFunctionProperty, BCryptQueryContextFunctionProperty function [Security], CRYPT_DOMAIN, CRYPT_LOCAL, NCRYPT_KEY_STORAGE_INTERFACE, NCRYPT_SCHANNEL_INTERFACE, bcrypt/BCryptQueryContextFunctionProperty, security.bcryptquerycontextfunctionproperty
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - BCryptQueryContextFunctionProperty
 - bcrypt/BCryptQueryContextFunctionProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
api_name:
 - BCryptQueryContextFunctionProperty
---

# BCryptQueryContextFunctionProperty function


## -description

The <b>BCryptQueryContextFunctionProperty</b> function obtains the value of a named property for a cryptographic function in an existing CNG context.

## -parameters

### -param dwTable [in]

Identifies the configuration table that the context exists in. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_LOCAL"></a><a id="crypt_local"></a><dl>
<dt><b>CRYPT_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The context exists in the local-machine configuration table.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DOMAIN"></a><a id="crypt_domain"></a><dl>
<dt><b>CRYPT_DOMAIN</b></dt>
</dl>
</td>
<td width="60%">
This value is not available for use.

</td>
</tr>
</table>

### -param pszContext [in]

A pointer to a null-terminated Unicode string that contains the identifier of the context to obtain the function property from.

### -param dwInterface [in]

Identifies the cryptographic interface that the function exists in. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE"></a><a id="bcrypt_asymmetric_encryption_interface"></a><dl>
<dt><b>BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The function exists in the list of asymmetric encryption functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_CIPHER_INTERFACE"></a><a id="bcrypt_cipher_interface"></a><dl>
<dt><b>BCRYPT_CIPHER_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The function exists in the list of cipher functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_HASH_INTERFACE"></a><a id="bcrypt_hash_interface"></a><dl>
<dt><b>BCRYPT_HASH_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The function exists in the list of hash functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RNG_INTERFACE"></a><a id="bcrypt_rng_interface"></a><dl>
<dt><b>BCRYPT_RNG_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The function exists in the list of random number generator functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></a><a id="bcrypt_secret_agreement_interface"></a><dl>
<dt><b>BCRYPT_SECRET_AGREEMENT_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The function exists in the list of secret agreement functions.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SIGNATURE_INTERFACE"></a><a id="bcrypt_signature_interface"></a><dl>
<dt><b>BCRYPT_SIGNATURE_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The function exists in the list of signature functions.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_KEY_STORAGE_INTERFACE"></a><a id="ncrypt_key_storage_interface"></a><dl>
<dt><b>NCRYPT_KEY_STORAGE_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The function exists in the list of key storage functions.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SCHANNEL_INTERFACE"></a><a id="ncrypt_schannel_interface"></a><dl>
<dt><b>NCRYPT_SCHANNEL_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The function exists in the list of Schannel functions.

</td>
</tr>
</table>

### -param pszFunction [in]

A pointer to a null-terminated Unicode string that contains the identifier of the cryptographic function to obtain the property for.

### -param pszProperty [in]

A pointer to a null-terminated Unicode string that contains the identifier of the property to obtain.

### -param pcbValue [in, out]

The address of a <b>ULONG</b> variable that, on entry, contains the size, in bytes, of the buffer pointed to by <i>ppbValue</i>. If this size is not large enough to hold the property value, this function will fail with <b>STATUS_BUFFER_TOO_SMALL</b>.

After this function returns, this variable contains the number of bytes that were copied to the <i>ppbValue</i> buffer.

### -param ppbValue [in, out]

The address of a pointer to a buffer that receives the property data. The size and format of this buffer depends on the format of the property being retrieved. The value pointed to by the <i>pcbValue</i> parameter contains the size of this buffer.

If the value pointed to by this parameter is <b>NULL</b>, this function will allocate the required memory. This memory must be freed when it is no longer needed by passing this pointer to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfreebuffer">BCryptFreeBuffer</a> function.

If this parameter is <b>NULL</b>, this function will place the required size, in bytes, in the variable pointed to by the <i>pcbValue</i> parameter and return <b>STATUS_BUFFER_TOO_SMALL</b>.

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
The <i>ppbValue</i> parameter is not <b>NULL</b>, and the value pointed to by the <i>pcbValue</i> parameter is not large enough to hold the set of contexts.

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
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified context, function, or property could not be found.

</td>
</tr>
</table>

## -remarks

<b>BCryptQueryContextFunctionProperty</b> can be called only in user mode.