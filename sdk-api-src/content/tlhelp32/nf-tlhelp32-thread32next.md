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

# Thread32Next function


## -description


Retrieves information about the next thread of any process encountered in the system memory snapshot.


## -parameters




### -param hSnapshot [in]

A handle to the snapshot returned from a previous call to the 
<a href="https://msdn.microsoft.com/df643c25-7558-424c-b187-b3f86ba51358">CreateToolhelp32Snapshot</a> function.


### -param lpte [out]

A pointer to a 
<a href="https://msdn.microsoft.com/923feca1-8807-4752-8a5a-79075688aabd">THREADENTRY32</a> structure.


## -returns



Returns <b>TRUE</b> if the next entry of the thread list has been copied to the buffer or <b>FALSE</b> otherwise. The <b>ERROR_NO_MORE_FILES</b> error value is returned by the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function if no threads exist or the snapshot does not contain thread information.




## -remarks



To retrieve information about the first thread recorded in a snapshot, use the 
<a href="https://msdn.microsoft.com/d4cb7a19-850e-43b5-bda5-91be48382d2a">Thread32First</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/67194627-8239-46d2-93e7-eb8e5f6c56e6">Traversing the Thread List</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/df643c25-7558-424c-b187-b3f86ba51358">CreateToolhelp32Snapshot</a>



<a href="https://msdn.microsoft.com/923feca1-8807-4752-8a5a-79075688aabd">THREADENTRY32</a>



<a href="https://msdn.microsoft.com/2440b781-652d-4d73-b173-87504e7b49b5">Thread Walking</a>



<a href="https://msdn.microsoft.com/d4cb7a19-850e-43b5-bda5-91be48382d2a">Thread32First</a>



<a href="https://msdn.microsoft.com/83732bd6-f4cf-409d-ad17-86503d408dc3">Tool Help Functions</a>
 

 

