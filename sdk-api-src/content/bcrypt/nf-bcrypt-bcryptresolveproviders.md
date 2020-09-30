---
UID: NF:bcrypt.BCryptResolveProviders
title: BCryptResolveProviders function (bcrypt.h)
description: Obtains a collection of all of the providers that meet the specified criteria.
helpviewer_keywords: ["BCryptResolveProviders","BCryptResolveProviders function [Security]","CRYPT_ALL_FUNCTIONS","CRYPT_ALL_PROVIDERS","CRYPT_KM","CRYPT_MM","CRYPT_UM","bcrypt/BCryptResolveProviders","security.bcryptresolveproviders"]
old-location: security\bcryptresolveproviders.htm
tech.root: security
ms.assetid: cf30f635-4918-4911-9db0-df90d26a2f1a
ms.date: 12/05/2018
ms.keywords: BCryptResolveProviders, BCryptResolveProviders function [Security], CRYPT_ALL_FUNCTIONS, CRYPT_ALL_PROVIDERS, CRYPT_KM, CRYPT_MM, CRYPT_UM, bcrypt/BCryptResolveProviders, security.bcryptresolveproviders
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
 - BCryptResolveProviders
 - bcrypt/BCryptResolveProviders
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
 - BCryptResolveProviders
---

# BCryptResolveProviders function


## -description

The <b>BCryptResolveProviders</b> function obtains a collection of all of the providers that meet the specified criteria.

## -parameters

### -param pszContext [in, optional]

A pointer to a null-terminated Unicode string that contains the identifier of the context for which to obtain the providers.  If this is set to <b>NULL</b> or to an empty string, the default context is assumed.

### -param dwInterface [in, optional]

The identifier of an interface that the provider must support. This must be one of the <a href="/windows/desktop/SecCNG/cng-interface-identifiers">CNG Interface Identifiers</a>. If the <i>pszFunction</i> parameter is not <b>NULL</b> or an empty string, you can set <i>dwInterface</i> to zero to force the function to infer the interface.

### -param pszFunction [in, optional]

A pointer to a null-terminated Unicode string that contains the algorithm or function identifier that the provider must support. This can be one of the standard <a href="/windows/desktop/SecCNG/cng-algorithm-identifiers">CNG Algorithm Identifiers</a> or the identifier for another registered algorithm.  If <i>dwInterface</i> is set to a nonzero value, then <i>pszFunction</i> can be <b>NULL</b> to include all algorithms and functions.

### -param pszProvider [in, optional]

A pointer to a null-terminated Unicode string that contains the name of the provider to retrieve. If this parameter is <b>NULL</b>, then all providers will be included.

This parameter allows you to specify a specific provider to retrieve in the event that more than one provider meets the other criteria.

### -param dwMode [in]

Specifies the type of provider to retrieve. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_UM"></a><a id="crypt_um"></a><dl>
<dt><b>CRYPT_UM</b></dt>
</dl>
</td>
<td width="60%">
Retrieve user mode providers.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_KM"></a><a id="crypt_km"></a><dl>
<dt><b>CRYPT_KM</b></dt>
</dl>
</td>
<td width="60%">
Retrieve kernel mode providers.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_MM"></a><a id="crypt_mm"></a><dl>
<dt><b>CRYPT_MM</b></dt>
</dl>
</td>
<td width="60%">
Retrieve both user mode and kernel mode providers.

</td>
</tr>
</table>

### -param dwFlags [in]

A set of flags that modify the behavior of this function.


This can be a zero or a combination of one or more of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ALL_FUNCTIONS"></a><a id="crypt_all_functions"></a><dl>
<dt><b>CRYPT_ALL_FUNCTIONS</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
This function will retrieve all of the functions supported by each provider that meets the specified criteria. If this flag is not specified, this function will only retrieve the first function of the provider or providers that meet the specified criteria.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ALL_PROVIDERS"></a><a id="crypt_all_providers"></a><dl>
<dt><b>CRYPT_ALL_PROVIDERS</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
This function will retrieve all of the providers that meet the specified criteria. If this flag is not specified, this function will only retrieve the first provider that is found that meets the specified criteria.

</td>
</tr>
</table>

### -param pcbBuffer [in, out]

A pointer to a <b>DWORD</b> value that, on entry, contains the size, in bytes, of the buffer pointed to by the <i>ppBuffer</i> parameter. On exit, this value receives either the number of bytes copied to the buffer or the required size, in bytes, of the buffer.

### -param ppBuffer [in, out]

The address of a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_provider_refs">CRYPT_PROVIDER_REFS</a> pointer that receives the collection of providers that meet the specified criteria.

If this parameter is <b>NULL</b>, this function will return <b>STATUS_SUCCESS</b> and place in the value pointed to by the <i>pcbBuffer</i> parameter, the required size, in bytes, of all the data.

If this parameter is the address of a <b>NULL</b> pointer, this function will allocate the required memory, fill the memory with the information about the providers, and place the pointer to this memory in this parameter. When you have finished using this memory,  free it by passing this pointer to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfreebuffer">BCryptFreeBuffer</a> function.

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
<dt><b>STATUS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No provider could be found that meets all of the specified criteria.

</td>
</tr>
</table>

## -remarks

<b>BCryptResolveProviders</b> can be called either from user mode or kernel mode. Kernel mode callers must be executing at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a>.