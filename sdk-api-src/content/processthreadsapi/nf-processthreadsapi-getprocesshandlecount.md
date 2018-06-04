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

# GetProcessHandleCount function


## -description


Retrieves the number of open handles  that belong to the specified process.


## -parameters




### -param hProcess [in]

A handle to the process whose handle count is being requested.  The
        handle must have the PROCESS_QUERY_INFORMATION
        or PROCESS_QUERY_LIMITED_INFORMATION access right. For more information, see <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the PROCESS_QUERY_INFORMATION access right.


### -param pdwHandleCount [in, out]

A pointer to a variable that receives the number of open handles that belong to the specified process.


## -returns



If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error  information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function retrieves information about the executive objects for the process. For more information, see <a href="https://msdn.microsoft.com/3e3288dd-155a-41d0-9d43-5f49ed4c4a9d">Kernel Objects</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>
 

 

