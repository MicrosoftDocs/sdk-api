---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# BCryptRegisterConfigChangeNotify function


## -description


<p class="CCE_Message">[<b>BCryptRegisterConfigChangeNotify</b> is deprecated beginning with Windows 10.]

The <b>BCryptRegisterConfigChangeNotify(HANDLE*)</b> function creates a user mode CNG configuration change event handler.


## -parameters




### -param pEvent

TBD




#### - phEvent [out]

The address of a <b>HANDLE</b> variable that receives the event handle. Use one of the <a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">Wait Functions</a>, such as <a href="https://msdn.microsoft.com/e37ebff7-b44e-469d-81ab-7a6bd1a0c822">WaitForSingleObject</a>, to determine when the event has been signaled. The event is unnamed and must be a manual-reset event. The event is signaled when any CNG configuration data has changed.

This handle must be passed to the <a href="https://msdn.microsoft.com/204d289d-46c0-4815-a628-758310014790">BCryptUnregisterConfigChangeNotify(HANDLE)</a> function to remove the event notification.


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

<b>BCryptRegisterConfigChangeNotify(HANDLE*)</b> can be called only in user mode. Code executing in kernel mode must call <a href="https://msdn.microsoft.com/ca30e81d-d384-4574-8394-42542a504218">BCryptRegisterConfigChangeNotify(PRKEVENT)</a>.




## -see-also




<a href="https://msdn.microsoft.com/204d289d-46c0-4815-a628-758310014790">BCryptUnregisterConfigChangeNotify(HANDLE)</a>
 

 

