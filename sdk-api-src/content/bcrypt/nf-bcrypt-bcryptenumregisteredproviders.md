---
UID: NF:bcrypt.BCryptEnumRegisteredProviders
title: BCryptEnumRegisteredProviders function (bcrypt.h)
description: Retrieves information about the registered providers.
helpviewer_keywords: ["BCryptEnumRegisteredProviders","BCryptEnumRegisteredProviders function [Security]","bcrypt/BCryptEnumRegisteredProviders","security.bcryptenumregisteredproviders"]
old-location: security\bcryptenumregisteredproviders.htm
tech.root: security
ms.assetid: a01adfec-dbe0-4817-af97-63163760fafc
ms.date: 12/05/2018
ms.keywords: BCryptEnumRegisteredProviders, BCryptEnumRegisteredProviders function [Security], bcrypt/BCryptEnumRegisteredProviders, security.bcryptenumregisteredproviders
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
 - BCryptEnumRegisteredProviders
 - bcrypt/BCryptEnumRegisteredProviders
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
 - BCryptEnumRegisteredProviders
---

# BCryptEnumRegisteredProviders function


## -description

The <b>BCryptEnumRegisteredProviders</b> function retrieves information about the registered providers.

## -parameters

### -param pcbBuffer [in, out]

A pointer to a <b>ULONG</b> value that, on entry, contains the size, in bytes, of the buffer pointed to by the <i>ppBuffer</i> parameter. On exit, this value receives either the number of bytes copied to the buffer or the required size, in bytes, of the buffer.

<div class="alert"><b>Note</b>  This is the total size, in bytes, of the entire buffer, not just the size of the <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_providers">CRYPT_PROVIDERS</a> structure. The buffer must be able to hold other data for the providers in addition to the <b>CRYPT_PROVIDERS</b> structure.</div>
<div> </div>

### -param ppBuffer [in, out]

A pointer to a buffer pointer that receives a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_providers">CRYPT_PROVIDERS</a> structure and other data that describes the collection of registered providers.

If this parameter is <b>NULL</b>, this function will return <b>STATUS_BUFFER_TOO_SMALL</b> and place in the value pointed to by the <i>pcbBuffer</i> parameter, the required size, in bytes, of all the data.

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
</table>

## -remarks

The <b>BCryptEnumRegisteredProviders</b> function can be called in one of two ways:

<ul>
<li>
The first is to have the <b>BCryptEnumRegisteredProviders</b> function allocate the memory. This is accomplished by passing the address of a <b>NULL</b> pointer for the <i>ppBuffer</i> parameter.

The following example shows how to use the <b>BCryptEnumRegisteredProviders</b> function to allocate memory by passing the address of a <b>NULL</b> pointer for the <i>ppBuffer</i> parameter.


```cpp
PCRYPT_PROVIDERS pBuffer = NULL;
BCryptEnumRegisteredProviders(/*...*/, &pBuffer);


```


This code will allocate the memory required for the <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_providers">CRYPT_PROVIDERS</a> structure and the associated strings. When the <b>BCryptEnumRegisteredProviders</b> function is used in this manner, you must free the memory when it is no longer needed by passing <i>ppBuffer</i> to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfreebuffer">BCryptFreeBuffer</a> function.

</li>
<li>The second method is to allocate the required memory yourself. This is accomplished by calling the <b>BCryptEnumRegisteredProviders</b> function with <b>NULL</b> for the <i>ppBuffer</i> parameter. The <b>BCryptEnumRegisteredProviders</b> function will place in the value pointed to by the <i>pcbBuffer</i> parameter, the required size, in bytes, of the <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_providers">CRYPT_PROVIDERS</a> structure and all strings. You then allocate the required memory and pass the address of this buffer pointer for the <i>ppBuffer</i> parameter in a second call to the <b>BCryptEnumRegisteredProviders</b> function.</li>
</ul>


<b>BCryptEnumRegisteredProviders</b> can be called only in user mode.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfreebuffer">BCryptFreeBuffer</a>



<a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_providers">CRYPT_PROVIDERS</a>