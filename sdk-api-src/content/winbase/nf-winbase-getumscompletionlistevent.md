---
UID: NF:winbase.GetUmsCompletionListEvent
title: GetUmsCompletionListEvent function
author: windows-sdk-content
description: Retrieves a handle to the event associated with the specified user-mode scheduling (UMS) completion list.
old-location: base\getumscompletionlistevent.htm
tech.root: procthread
ms.assetid: 393f6e0a-fbea-4aa0-9c18-f96da18e61e9
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetUmsCompletionListEvent, GetUmsCompletionListEvent function, base.getumscompletionlistevent, winbase/GetUmsCompletionListEvent
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
 - kernel32.dll
 - API-MS-Win-Core-ums-l1-1-0.dll
api_name:
 - GetUmsCompletionListEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetUmsCompletionListEvent function


## -description


Retrieves a handle to the event associated with the specified user-mode scheduling (UMS) completion list. 


## -parameters




### -param UmsCompletionList [in]

A pointer to a UMS completion list. The <a href="https://msdn.microsoft.com/6e77b793-a82e-4e23-8c8b-7aff79d69346">CreateUmsCompletionList</a> function provides this pointer.


### -param UmsCompletionEvent [in, out]

A pointer to a HANDLE variable. On output, the <i>UmsCompletionEvent</i> parameter is set to a handle to the event associated with the specified completion list.


## -returns



If the function succeeds, it returns a nonzero value.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The system signals a UMS completion list event when the system queues items to an empty completion list. A completion list event handle can be used with any <a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait function</a> that takes a handle to an event. When the event is signaled, an application typically calls <a href="https://msdn.microsoft.com/91499eb9-9fc5-4135-95f6-1bced78f1e07">DequeueUmsCompletionListItems</a> to retrieve the contents of the completion list. 

The event handle remains valid until its completion list is deleted. Do not use the event handle to wait on a completion list that has been deleted or is in the process of being deleted.

When the handle is no longer needed, use the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the handle.




## -see-also




<a href="https://msdn.microsoft.com/6e77b793-a82e-4e23-8c8b-7aff79d69346">CreateUmsCompletionList</a>



<a href="https://msdn.microsoft.com/91499eb9-9fc5-4135-95f6-1bced78f1e07">DequeueUmsCompletionListItems</a>



<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">Wait Functions</a>
 

 

