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

# CloseThreadpoolIo function


## -description


Releases the specified I/O completion object.


## -parameters




### -param pio [in, out]

A <b>TP_IO</b> structure that defines the I/O completion object. The <a href="https://msdn.microsoft.com/621f4747-50fa-4538-bd6a-dbe4dbb05dd1">CreateThreadpoolIo</a> function returns this structure.


## -returns



This function does not return a value.




## -remarks



The I/O completion object is freed immediately if there are no outstanding callbacks; otherwise, the I/O completion object is freed asynchronously after the outstanding callbacks complete. 

You should close the associated file handle and wait for all outstanding overlapped I/O operations to complete before calling this function—you must not cause any more overlapped I/O operations to occur after calling this function.

It may be necessary to cancel threadpool I/O notifications to prevent memory leaks. For more information, see <a href="https://msdn.microsoft.com/e3af8313-2e09-4c88-8cef-671efd4228c7">CancelThreadpoolIo</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.




## -see-also




<a href="https://msdn.microsoft.com/e3af8313-2e09-4c88-8cef-671efd4228c7">CancelThreadpoolIo</a>



<a href="https://msdn.microsoft.com/621f4747-50fa-4538-bd6a-dbe4dbb05dd1">CreateThreadpoolIo</a>



<a href="https://msdn.microsoft.com/5a817d6f-a8e6-4aaa-b560-0128eacb98b1">StartThreadpoolIo</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>



<a href="https://msdn.microsoft.com/68dc640d-8678-441d-88bd-01284d98a251">WaitForThreadpoolIoCallbacks</a>
 

 

