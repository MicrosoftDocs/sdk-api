---
UID: NF:bcrypt.BCryptQueryProviderRegistration
title: BCryptQueryProviderRegistration function (bcrypt.h)
description: Retrieves information about a CNG provider.
helpviewer_keywords: ["BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE","BCRYPT_CIPHER_INTERFACE","BCRYPT_HASH_INTERFACE","BCRYPT_RNG_INTERFACE","BCRYPT_SECRET_AGREEMENT_INTERFACE","BCRYPT_SIGNATURE_INTERFACE","BCryptQueryProviderRegistration","BCryptQueryProviderRegistration function [Security]","CRYPT_ANY","CRYPT_KM","CRYPT_MM","CRYPT_UM","NCRYPT_KEY_STORAGE_INTERFACE","NCRYPT_SCHANNEL_INTERFACE","bcrypt/BCryptQueryProviderRegistration","security.bcryptqueryproviderregistration"]
old-location: security\bcryptqueryproviderregistration.htm
tech.root: security
ms.assetid: 28b8bca9-442f-4d58-86aa-8aa274777ede
ms.date: 12/05/2018
ms.keywords: BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE, BCRYPT_CIPHER_INTERFACE, BCRYPT_HASH_INTERFACE, BCRYPT_RNG_INTERFACE, BCRYPT_SECRET_AGREEMENT_INTERFACE, BCRYPT_SIGNATURE_INTERFACE, BCryptQueryProviderRegistration, BCryptQueryProviderRegistration function [Security], CRYPT_ANY, CRYPT_KM, CRYPT_MM, CRYPT_UM, NCRYPT_KEY_STORAGE_INTERFACE, NCRYPT_SCHANNEL_INTERFACE, bcrypt/BCryptQueryProviderRegistration, security.bcryptqueryproviderregistration
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
 - BCryptQueryProviderRegistration
 - bcrypt/BCryptQueryProviderRegistration
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
 - BCryptQueryProviderRegistration
---

# BCryptQueryProviderRegistration function


## -description

The <b>BCryptQueryProviderRegistration</b> function retrieves information about a CNG provider.

## -parameters

### -param pszProvider [in]

A pointer to a null-terminated Unicode string that contains the name of the provider to obtain information about.

### -param dwMode [in]

Specifies the type of information to retrieve. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ANY"></a><a id="crypt_any"></a><dl>
<dt><b>CRYPT_ANY</b></dt>
</dl>
</td>
<td width="60%">
Retrieve any information for the provider.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_UM"></a><a id="crypt_um"></a><dl>
<dt><b>CRYPT_UM</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the user mode information for the provider.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_KM"></a><a id="crypt_km"></a><dl>
<dt><b>CRYPT_KM</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the kernel mode information for the provider.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_MM"></a><a id="crypt_mm"></a><dl>
<dt><b>CRYPT_MM</b></dt>
</dl>
</td>
<td width="60%">
Retrieve both the user mode and kernel mode information for the provider.

</td>
</tr>
</table>

### -param dwInterface [in]

Specifies the interface to retrieve information for. This can be one of the following values.

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
Retrieve the asymmetric encryption interface.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_CIPHER_INTERFACE"></a><a id="bcrypt_cipher_interface"></a><dl>
<dt><b>BCRYPT_CIPHER_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the cipher interface.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_HASH_INTERFACE"></a><a id="bcrypt_hash_interface"></a><dl>
<dt><b>BCRYPT_HASH_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the hash interface.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_KEY_STORAGE_INTERFACE"></a><a id="ncrypt_key_storage_interface"></a><dl>
<dt><b>NCRYPT_KEY_STORAGE_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the key storage interface.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RNG_INTERFACE"></a><a id="bcrypt_rng_interface"></a><dl>
<dt><b>BCRYPT_RNG_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the random number generator interface.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SCHANNEL_INTERFACE"></a><a id="ncrypt_schannel_interface"></a><dl>
<dt><b>NCRYPT_SCHANNEL_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the Schannel interface.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></a><a id="bcrypt_secret_agreement_interface"></a><dl>
<dt><b>BCRYPT_SECRET_AGREEMENT_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the secret agreement interface.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SIGNATURE_INTERFACE"></a><a id="bcrypt_signature_interface"></a><dl>
<dt><b>BCRYPT_SIGNATURE_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the signature interface.

</td>
</tr>
</table>

### -param pcbBuffer [in, out]

A pointer to a <b>ULONG</b> value that, on entry, contains the size, in bytes, of the buffer pointed to by the <i>ppBuffer</i> parameter. On exit, this value receives either the number of bytes copied to the buffer or the required size, in bytes, of the buffer.


<div class="alert"><b>Note</b>  This is the total size, in bytes, of the entire buffer, not just the size of the <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_provider_reg">CRYPT_PROVIDER_REG</a> structure. The buffer must be able to hold other data for the providers in addition to the <b>CRYPT_PROVIDER_REG</b> structure.</div>
<div> </div>

### -param ppBuffer [in, out]

A pointer to a buffer pointer that receives a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_provider_reg">CRYPT_PROVIDER_REG</a> structure and other data that describes the provider.

If this parameter is <b>NULL</b>, this function will return <b>STATUS_BUFFER_TOO_SMALL</b> and place in the value pointed to by the <i>pcbBuffer</i> parameter, the required size, in bytes, of all data.

If this parameter is the address of a <b>NULL</b> pointer, this function will allocate the required memory, fill it in with the provider information, and place a pointer to this memory in this parameter. When you have finished using this memory, free it by passing this pointer to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfreebuffer">BCryptFreeBuffer</a> function.

If this parameter is the address of a non-<b>NULL</b> pointer, this function will copy the provider information into this buffer. The <i>pcbBuffer</i> parameter must contain the size, in bytes, of the entire buffer. If the buffer is not large enough to hold all of the provider information, this function will return <b>STATUS_BUFFER_TOO_SMALL</b>.

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
<dt><b>STATUS_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The size specified by the <i>pcbBuffer</i> parameter is not large enough to hold all of the data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No provider could be found that matches the specified criteria.

</td>
</tr>
</table>

## -remarks

<b>BCryptQueryProviderRegistration</b> can be called only in user mode.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfreebuffer">BCryptFreeBuffer</a>



<a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_provider_reg">CRYPT_PROVIDER_REG</a>