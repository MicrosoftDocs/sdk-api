---
UID: NF:bcrypt.BCryptUnregisterConfigChangeNotify
title: BCryptUnregisterConfigChangeNotify function
author: windows-sdk-content
description: Removes a user mode CNG configuration change event handler that was created by using the BCryptRegisterConfigChangeNotify(HANDLE*) function.
old-location: security\bcryptunregisterconfigchangenotify_handle.htm
tech.root: SecCNG
ms.assetid: 204d289d-46c0-4815-a628-758310014790
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: BCryptUnregisterConfigChangeNotify, BCryptUnregisterConfigChangeNotify function [Security], BCryptUnregisterConfigChangeNotify(HANDLE), bcrypt/BCryptUnregisterConfigChangeNotify, security.bcryptunregisterconfigchangenotify_handle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
api_name:
 - BCryptUnregisterConfigChangeNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BCryptUnregisterConfigChangeNotify function


## -description


The <b>BCryptUnregisterConfigChangeNotify(HANDLE)</b> function removes a user mode CNG configuration change event handler that was created by using the <a href="https://msdn.microsoft.com/e0d60ea1-3b0b-4afe-bbfc-52f0d48b7399">BCryptRegisterConfigChangeNotify(HANDLE*)</a> function.


## -parameters




### -param pEvent [in]

The handle of the event to remove. This is the handle that was obtained by using the <a href="https://msdn.microsoft.com/e0d60ea1-3b0b-4afe-bbfc-52f0d48b7399">BCryptRegisterConfigChangeNotify(HANDLE*)</a> function.


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



<b>BCryptUnregisterConfigChangeNotify(HANDLE)</b> can be called only in user mode. Code executing in kernel mode must call <a href="https://msdn.microsoft.com/6354f595-f917-485e-8682-2be994135c36">BCryptUnregisterConfigChangeNotify(PRKEVENT)</a>.




## -see-also




<a href="https://msdn.microsoft.com/e0d60ea1-3b0b-4afe-bbfc-52f0d48b7399">BCryptRegisterConfigChangeNotify(HANDLE*)</a>
 

 

