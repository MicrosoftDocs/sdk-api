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

# BCryptUnregisterConfigChangeNotify function


## -description


The <b>BCryptUnregisterConfigChangeNotify(HANDLE)</b> function removes a user mode CNG configuration change event handler that was created by using the <a href="https://msdn.microsoft.com/e0d60ea1-3b0b-4afe-bbfc-52f0d48b7399">BCryptRegisterConfigChangeNotify(HANDLE*)</a> function.


## -parameters




### -param pEvent

TBD




#### - hEvent [in]

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
 

 

