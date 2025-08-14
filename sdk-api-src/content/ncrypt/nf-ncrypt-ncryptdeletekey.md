---
UID: NF:ncrypt.NCryptDeleteKey
title: NCryptDeleteKey function (ncrypt.h)
description: Deletes a CNG key from storage.
helpviewer_keywords: ["NCRYPT_SILENT_FLAG","NCryptDeleteKey","NCryptDeleteKey function [Security]","ncrypt/NCryptDeleteKey","security.ncryptdeletekey_func"]
old-location: security\ncryptdeletekey_func.htm
tech.root: security
ms.assetid: 2e1958a7-51e0-4731-b4cf-a90d6c1f9ae0
ms.date: 12/05/2018
ms.keywords: NCRYPT_SILENT_FLAG, NCryptDeleteKey, NCryptDeleteKey function [Security], ncrypt/NCryptDeleteKey, security.ncryptdeletekey_func
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
 - NCryptDeleteKey
 - ncrypt/NCryptDeleteKey
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
 - NCryptDeleteKey
---

# NCryptDeleteKey function


## -description

The <b>NCryptDeleteKey</b> function deletes a CNG key.

## -parameters

### -param hKey [in]

The handle of the key to delete. This handle is obtained by using the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptopenkey">NCryptOpenKey</a> function.

<div class="alert"><b>Note</b>  The <b>NCryptDeleteKey</b> function deletes the key and frees the handle. Applications may use <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptfreeobject">NCryptFreeObject</a> function to free the handle if <b>NCryptDeleteKey</b> fails.</div>
<div> </div>

### -param dwFlags [in]

Flags that modify function behavior. This can be zero or a combination of values that is specific to each key storage provider.

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
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hKey</i> parameter is not valid.

</td>
</tr>
</table>

## -remarks

A service must not call this function from its <a href="/windows/win32/api/winsvc/nf-winsvc-startservicea">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.

## -see-also

<a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptopenkey">NCryptOpenKey</a>
