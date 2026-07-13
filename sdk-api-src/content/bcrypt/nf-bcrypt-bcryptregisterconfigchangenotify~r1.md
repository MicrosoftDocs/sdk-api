---
UID: NF:bcrypt.BCryptRegisterConfigChangeNotify~r1
title: BCryptRegisterConfigChangeNotify
description: Describes how the BCryptRegisterConfigChangeNotify(PRKEVENT) function creates kernel mode CNG configuration change event handler.
ms.date: 08/01/2022
ms.keywords: BCryptRegisterConfigChangeNotify
targetos: Windows
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
ms.custom: 19H1
f1_keywords:
 - BCryptRegisterConfigChangeNotify
 - bcrypt/BCryptRegisterConfigChangeNotify
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - bcrypt.h
api_name:
 - BCryptRegisterConfigChangeNotify
---

# BCryptRegisterConfigChangeNotify function


## -description

<p class="CCE_Message">[<b>BCryptRegisterConfigChangeNotify</b> is deprecated beginning with Windows 10.]

The <b>BCryptRegisterConfigChangeNotify(PRKEVENT)</b> function creates kernel mode CNG configuration change event handler.

## -parameters

### -param phEvent [in]

The address of a <b>PRKEVENT</b> variable that receives the pointer to the event dispatcher object. 
You use the kernel wait functions, such as <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>, to determine when the event has been signaled. 
The event is signaled when the CNG configuration has changed.

This handle must be passed to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptunregisterconfigchangenotify">BCryptUnregisterConfigChangeNotify(PRKEVENT)</a> function to remove the event notification.

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
The <i>phEvent</i> parameter is not valid.

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

The handle returned in the variable pointed to by the <i>phEvent</i> parameter will be signaled when a change to the CNG configuration occurs.

<b>BCryptRegisterConfigChangeNotify(HANDLE*)</b> can be called only in user mode. Code executing in kernel mode must call <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptregisterconfigchangenotify">BCryptRegisterConfigChangeNotify(PRKEVENT)</a>.
<b>BCryptRegisterConfigChangeNotify(PRKEVENT)</b> can be called only in kernel mode and at <b>PASSIVE_LEVEL</b> IRQL. 
Code executing in user mode must call <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptregisterconfigchangenotify">BCryptRegisterConfigChangeNotify(HANDLE*)</a>.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptunregisterconfigchangenotify">BCryptUnregisterConfigChangeNotify(PRKEVENT) function</a>
