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

# ShutdownBlockReasonCreate function


## -description


Indicates that the system cannot be shut down and sets a reason string to be displayed to the user if system shutdown is initiated.


## -parameters




### -param hWnd [in]

A handle to the main window of the application.


### -param pwszReason [in]

The reason the application must block system shutdown. This string will be truncated for display purposes after MAX_STR_BLOCKREASON characters.


## -returns



If the call succeeds, the return value is nonzero.

If the call fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function can only be called from the thread that created the window specified by the <i>hWnd</i> parameter. Otherwise, the function fails and the last error code is ERROR_ACCESS_DENIED.

Applications should call this function as they begin an operation that cannot be interrupted, such as burning a CD or DVD. When the operation has completed, call the <a href="https://msdn.microsoft.com/b7bf376a-79b5-4f63-b3ca-0d515c23d67c">ShutdownBlockReasonDestroy</a> function to indicate that the system can be shut down.

Because users are typically in a hurry when shutting down the system, they may spend only  a few seconds looking at the shutdown reasons that are displayed by the system. Therefore, it is important that your reason strings are short and clear. For example "A CD burn is in progress." is better than "This application is blocking system shutdown because a CD burn is in progress. Do not shut down."




## -see-also




<a href="https://msdn.microsoft.com/b7bf376a-79b5-4f63-b3ca-0d515c23d67c">ShutdownBlockReasonDestroy</a>



<a href="https://msdn.microsoft.com/acadf58f-3f68-4fa1-bdcf-8f85c8479263">Shutting Down</a>
 

 

