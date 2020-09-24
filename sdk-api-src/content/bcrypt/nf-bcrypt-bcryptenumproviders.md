---
UID: NF:bcrypt.BCryptEnumProviders
title: BCryptEnumProviders function (bcrypt.h)
description: Obtains all of the CNG providers that support a specified algorithm.
helpviewer_keywords: ["BCryptEnumProviders","BCryptEnumProviders function [Security]","bcrypt/BCryptEnumProviders","security.bcryptenumproviders_func"]
old-location: security\bcryptenumproviders_func.htm
tech.root: security
ms.assetid: 0496f241-9530-47fb-89e2-15d7ab6da87a
ms.date: 12/05/2018
ms.keywords: BCryptEnumProviders, BCryptEnumProviders function [Security], bcrypt/BCryptEnumProviders, security.bcryptenumproviders_func
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
 - BCryptEnumProviders
 - bcrypt/BCryptEnumProviders
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
 - BCryptEnumProviders
---

# BCryptEnumProviders function


## -description

The <b>BCryptEnumProviders</b> function obtains all of the CNG providers that support a specified algorithm.

## -parameters

### -param pszAlgId [in]

A pointer to a null-terminated Unicode string that identifies the algorithm to obtain the providers for. This can be one of the predefined <a href="/windows/desktop/SecCNG/cng-algorithm-identifiers">CNG Algorithm Identifiers</a> or another algorithm identifier.

### -param pImplCount [out]

A pointer to a <b>ULONG</b> variable to receive the number of elements in the <i>ppImplList</i> array.

### -param ppImplList [out]

The address of an array of <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_provider_name">BCRYPT_PROVIDER_NAME</a> structures to receive the collection of providers that support the specified algorithm. The <i>pImplCount</i> parameter receives the number of elements in this array. This memory must be freed when it is no longer needed by passing this pointer to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfreebuffer">BCryptFreeBuffer</a> function.

### -param dwFlags [in]

A set of flags that modifies the behavior of this function. There are currently no flags defined, so this parameter must be zero.

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
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -remarks

<b>BCryptEnumProviders</b> can be called either from user mode or kernel mode. Kernel mode callers must be executing at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a>.

## -see-also

<a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_provider_name">BCRYPT_PROVIDER_NAME</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfreebuffer">BCryptFreeBuffer</a>