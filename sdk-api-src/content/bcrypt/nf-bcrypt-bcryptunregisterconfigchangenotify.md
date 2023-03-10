---
UID: NF:bcrypt.BCryptUnregisterConfigChangeNotify
title: BCryptUnregisterConfigChangeNotify function (bcrypt.h)
description: Removes a user mode CNG configuration change event handler that was created by using the BCryptRegisterConfigChangeNotify(HANDLE*) function.
helpviewer_keywords: ["BCryptUnregisterConfigChangeNotify","BCryptUnregisterConfigChangeNotify function [Security]","BCryptUnregisterConfigChangeNotify(HANDLE)","bcrypt/BCryptUnregisterConfigChangeNotify","security.bcryptunregisterconfigchangenotify_handle"]
old-location: security\bcryptunregisterconfigchangenotify_handle.htm
tech.root: security
ms.assetid: 204d289d-46c0-4815-a628-758310014790
ms.date: 12/05/2018
ms.keywords: BCryptUnregisterConfigChangeNotify, BCryptUnregisterConfigChangeNotify function [Security], BCryptUnregisterConfigChangeNotify(HANDLE), bcrypt/BCryptUnregisterConfigChangeNotify, security.bcryptunregisterconfigchangenotify_handle
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
 - BCryptUnregisterConfigChangeNotify
 - bcrypt/BCryptUnregisterConfigChangeNotify
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
 - BCryptUnregisterConfigChangeNotify
---

# BCryptUnregisterConfigChangeNotify function


## -description

The <b>BCryptUnregisterConfigChangeNotify(HANDLE)</b> function removes a user mode CNG configuration change event handler that was created by using the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptregisterconfigchangenotify">BCryptRegisterConfigChangeNotify(HANDLE*)</a> function.

## -parameters

### -param pEvent [in]

The handle of the event to remove. This is the handle that was obtained by using the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptregisterconfigchangenotify">BCryptRegisterConfigChangeNotify(HANDLE*)</a> function.

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
The <i>hEvent</i> parameter is not valid.

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

<b>BCryptUnregisterConfigChangeNotify(HANDLE)</b> can be called only in user mode. Code executing in kernel mode must call <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptunregisterconfigchangenotify">BCryptUnregisterConfigChangeNotify(PRKEVENT)</a>.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptregisterconfigchangenotify">BCryptRegisterConfigChangeNotify(HANDLE*)</a>