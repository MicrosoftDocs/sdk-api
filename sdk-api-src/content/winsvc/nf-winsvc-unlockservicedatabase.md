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

# UnlockServiceDatabase function


## -description


<p class="CCE_Message">[This function has no effect as of Windows Vista.]

Unlocks a service control manager database by releasing the specified lock.


## -parameters




### -param ScLock [in]

The lock, which is obtained from a previous call to the 
<a href="https://msdn.microsoft.com/87861465-c966-479a-b906-27ae36cc83c8">LockServiceDatabase</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following error codes can be set by the service control manager. Other error codes can be set by the registry functions that are called by the service control manager.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SERVICE_LOCK</b></dt>
</dl>
</td>
<td width="60%">
The specified lock is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/87861465-c966-479a-b906-27ae36cc83c8">LockServiceDatabase</a>



<a href="https://msdn.microsoft.com/5139d31b-65f1-41ba-852a-91eab1dc366e">QueryServiceLockStatus</a>



<a href="https://msdn.microsoft.com/fc8c631e-076c-4745-8db0-90f46a202e6a">Service Configuration</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>
 

 

