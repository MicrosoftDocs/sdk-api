---
UID: NF:ncrypt.NCryptEnumKeys
title: NCryptEnumKeys function (ncrypt.h)
description: Obtains the names of the keys that are stored by the provider.
helpviewer_keywords: ["NCRYPT_MACHINE_KEY_FLAG","NCRYPT_SILENT_FLAG","NCryptEnumKeys","NCryptEnumKeys function [Security]","ncrypt/NCryptEnumKeys","security.ncryptenumkeys_func"]
old-location: security\ncryptenumkeys_func.htm
tech.root: security
ms.assetid: ca8c5b70-ea5e-4fb9-82d3-1de839f0d244
ms.date: 12/05/2018
ms.keywords: NCRYPT_MACHINE_KEY_FLAG, NCRYPT_SILENT_FLAG, NCryptEnumKeys, NCryptEnumKeys function [Security], ncrypt/NCryptEnumKeys, security.ncryptenumkeys_func
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
 - NCryptEnumKeys
 - ncrypt/NCryptEnumKeys
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
 - NCryptEnumKeys
---

# NCryptEnumKeys function


## -description

The <b>NCryptEnumKeys</b> function obtains the names of the keys that are stored by the provider.

## -parameters

### -param hProvider [in]

The handle of the key storage provider to enumerate the keys for. This handle is obtained with the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptopenstorageprovider">NCryptOpenStorageProvider</a> function.

### -param pszScope [in, optional]

This parameter is not currently used and must be <b>NULL</b>.

### -param ppKeyName [out]

The address of a pointer to an <a href="/windows/desktop/api/ncrypt/ns-ncrypt-ncryptkeyname">NCryptKeyName</a> structure that receives the name of the retrieved key. When the application has finished using this memory, free it by calling the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptfreebuffer">NCryptFreeBuffer</a> function.

### -param ppEnumState [in, out]

The address of a <b>VOID</b> pointer that receives enumeration state information that is used in subsequent calls to this function. This information only has meaning to the key storage provider and is opaque to the caller. The key storage provider uses this information to determine which item is next in the enumeration. If the variable pointed to by this parameter contains <b>NULL</b>, the enumeration is started from the beginning.

When this memory is no longer needed, it must be freed by passing this pointer to the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptfreebuffer">NCryptFreeBuffer</a> function.

### -param dwFlags [in]

Flags that modify function behavior. This can be zero or a combination of one or more of the following values.

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
Enumerate the keys for the local computer. If this flag is not present, the current user keys are enumerated.

</td>
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
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
The end of the enumeration has been reached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_SILENT_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter contains the <b>NCRYPT_SILENT_FLAG</b> flag, but the key being enumerated requires user interaction.

</td>
</tr>
</table>

## -remarks

This function retrieves only one item each time it is called. The state of the enumeration is stored in the variable pointed to by the <i>ppEnumState</i> parameter, so this must be preserved between calls to this function. When the last key stored by the provider has been retrieved, this function will return <b>NTE_NO_MORE_ITEMS</b> the next time it is called. To start the enumeration over, set the variable pointed to by the <i>ppEnumState</i> parameter to <b>NULL</b>, free the memory pointed to by the <i>ppKeyName</i> parameter, if it is not <b>NULL</b>, and call this function again.

A service must not call this function from its <a href="/windows/win32/api/winsvc/nf-winsvc-startservicea">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.