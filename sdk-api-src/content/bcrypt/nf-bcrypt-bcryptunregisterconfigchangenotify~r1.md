---
UID: NF:bcrypt.BCryptUnregisterConfigChangeNotify~r1
title: BCryptUnregisterConfigChangeNotify
description: Removes a user mode CNG configuration change event handler that was created by using the BCryptRegisterConfigChangeNotify(HANDLE*) function.
ms.date: 01/30/2019
ms.keywords: BCryptUnregisterConfigChangeNotify
ms.topic: language-reference
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: bcrypt.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: bcrypt.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
req.typenames: 
f1_keywords:
 - BCryptUnregisterConfigChangeNotify
 - bcrypt/BCryptUnregisterConfigChangeNotify
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - bcrypt.h
api_name:
 - BCryptUnregisterConfigChangeNotify
product: Windows
targetos: Windows
---

# BCryptUnregisterConfigChangeNotify function


## -description

The <b>BCryptUnregisterConfigChangeNotify(PRKEVENT)</b> function removes a kernel mode CNG configuration change event handler that was created by using the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptregisterconfigchangenotify">BCryptRegisterConfigChangeNotify(PRKEVENT)</a> function.

## -parameters

### -param hEvent

The pointer to the event dispatcher object to remove. 
This is the pointer that was obtained by using the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptregisterconfigchangenotify">BCryptRegisterConfigChangeNotify(PRKEVENT)</a> function.

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

<b>BCryptUnregisterConfigChangeNotify(PRKEVENT)</b> can be called only in kernel mode and at <b>PASSIVE_LEVEL</b> IRQL. 
Code executing in user mode must call <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptregisterconfigchangenotify">BCryptUnregisterConfigChangeNotify(HANDLE)</a>.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptregisterconfigchangenotify">BCryptRegisterConfigChangeNotify(PRKEVENT)</a>
