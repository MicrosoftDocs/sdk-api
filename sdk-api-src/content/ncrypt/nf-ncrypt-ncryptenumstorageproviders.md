---
UID: NF:ncrypt.NCryptEnumStorageProviders
title: NCryptEnumStorageProviders function (ncrypt.h)
description: Obtains the names of the registered key storage providers.
helpviewer_keywords: ["NCRYPT_SILENT_FLAG","NCryptEnumStorageProviders","NCryptEnumStorageProviders function [Security]","ncrypt/NCryptEnumStorageProviders","security.ncryptenumstorageproviders_func"]
old-location: security\ncryptenumstorageproviders_func.htm
tech.root: security
ms.assetid: 24a8ee01-b716-4f36-9df5-b6476b1df4f0
ms.date: 12/05/2018
ms.keywords: NCRYPT_SILENT_FLAG, NCryptEnumStorageProviders, NCryptEnumStorageProviders function [Security], ncrypt/NCryptEnumStorageProviders, security.ncryptenumstorageproviders_func
req.header: ncrypt.h
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
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptEnumStorageProviders
 - ncrypt/NCryptEnumStorageProviders
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
 - NCryptEnumStorageProviders
---

# NCryptEnumStorageProviders function


## -description

The <b>NCryptEnumStorageProviders</b> function obtains the names of the registered key storage providers.

## -parameters

### -param pdwProviderCount [out]

The address of a <b>DWORD</b> to receive the number of elements in the <i>ppProviderList</i> array.

### -param ppProviderList [out]

The address of an <a href="/windows/desktop/api/ncrypt/ns-ncrypt-ncryptprovidername">NCryptProviderName</a> structure pointer to receive an array of the registered key storage provider names. The variable pointed to by the <i>pdwProviderCount</i> parameter receives the number of elements in this array.

When this memory is no longer needed, free it by passing this pointer to the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptfreebuffer">NCryptFreeBuffer</a> function.

### -param dwFlags [in]

Flags that modify function behavior. This can be zero (0) or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SILENT_FLAG"></a><a id="ncrypt_silent_flag"></a><dl>
<dt><b>NCRYPT_SILENT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Requests that the key storage provider (KSP) not display any user interface. If the provider must display the UI to operate, the call fails and the KSP should set the <b>NTE_SILENT_CONTEXT</b> error code as the last error.

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

A service must not call this function from its <a href="/windows/win32/api/winsvc/nf-winsvc-startservicea">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.

## -see-also

<a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptfreebuffer">NCryptFreeBuffer</a>