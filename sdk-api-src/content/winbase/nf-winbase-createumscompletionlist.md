---
UID: NF:winbase.CreateUmsCompletionList
title: CreateUmsCompletionList function
author: windows-sdk-content
description: Creates a user-mode scheduling (UMS) completion list.
old-location: base\createumscompletionlist.htm
tech.root: procthread
ms.assetid: 6e77b793-a82e-4e23-8c8b-7aff79d69346
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateUmsCompletionList, CreateUmsCompletionList function, base.createumscompletionlist, winbase/CreateUmsCompletionList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 (64-bit only) [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ums-l1-1-0.dll
api_name:
 - CreateUmsCompletionList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

