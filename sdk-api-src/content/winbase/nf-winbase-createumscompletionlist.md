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

# CreateUmsCompletionList function


## -description


Creates a user-mode scheduling (UMS) completion list.


## -parameters




### -param UmsCompletionList [out]

A <b>PUMS_COMPLETION_LIST</b> variable. On output, this parameter receives a pointer 
      to an empty UMS completion list.


## -returns



If the function succeeds, it returns a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible error values include the 
       following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available to create the completion list.

</td>
</tr>
</table>
 




## -remarks



A completion list is associated with a UMS scheduler thread when the 
    <a href="https://msdn.microsoft.com/792bd7fa-0ae9-4c38-a664-5fb3e3d0c52b">EnterUmsSchedulingMode</a> function is called to 
     create the scheduler thread. The system queues newly created UMS worker threads to the completion list. It also 
     queues previously blocked UMS worker threads to the completion list when the threads are no longer blocked.

When an application's <a href="https://msdn.microsoft.com/10de1c48-255d-45c3-acf0-25f8a564b585">UmsSchedulerProc</a> entry 
     point function is called, the application's scheduler should retrieve items from the completion list by calling 
     <a href="https://msdn.microsoft.com/91499eb9-9fc5-4135-95f6-1bced78f1e07">DequeueUmsCompletionListItems</a>.

Each completion list has an associated completion list event which is signaled whenever the system queues 
     items to an empty list. Use the 
     <a href="https://msdn.microsoft.com/393f6e0a-fbea-4aa0-9c18-f96da18e61e9">GetUmsCompletionListEvent</a> to obtain a 
     handle to the event for a specified completion list.

When a completion list is no longer needed, use the 
     <a href="https://msdn.microsoft.com/98124359-ddd1-468c-9f99-74dd3f631fa1">DeleteUmsCompletionList</a> to release the list. 
     The list must be empty before it can be released.




## -see-also




<a href="https://msdn.microsoft.com/91499eb9-9fc5-4135-95f6-1bced78f1e07">DequeueUmsCompletionListItems</a>



<a href="https://msdn.microsoft.com/792bd7fa-0ae9-4c38-a664-5fb3e3d0c52b">EnterUmsSchedulingMode</a>



<a href="https://msdn.microsoft.com/393f6e0a-fbea-4aa0-9c18-f96da18e61e9">GetUmsCompletionListEvent</a>
 

 

