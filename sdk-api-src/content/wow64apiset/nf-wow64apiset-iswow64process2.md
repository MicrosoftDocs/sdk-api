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

# IsWow64Process2 function


## -description


Determines whether the specified process is running under 
<a href="https://msdn.microsoft.com/ac75c5af-86e8-4282-9a8e-8db3c22cbda0">WOW64</a>; also returns additional machine process and architecture information.


## -parameters




### -param hProcess [in]

A handle to the process. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


### -param pProcessMachine [out]

On success, returns a pointer to an <a href="https://msdn.microsoft.com/1E5E4F98-925B-424D-9B3D-BC6716FBF990">IMAGE_FILE_MACHINE_*</a> value. The value will be  <b>IMAGE_FILE_MACHINE_UNKNOWN</b> if the target process is not a <a href="https://msdn.microsoft.com/ac75c5af-86e8-4282-9a8e-8db3c22cbda0">WOW64</a> process; otherwise, it will identify the type of WoW process. 


### -param pNativeMachine [out, optional]

On success, returns a pointer to a possible <a href="https://msdn.microsoft.com/1E5E4F98-925B-424D-9B3D-BC6716FBF990">IMAGE_FILE_MACHINE_*</a> value identifying the native architecture of host system. 



## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>IsWow64Process2</b> provides an improved direct replacement for IsWow64Process. In addition to determining if the specified process is running under <a href="https://msdn.microsoft.com/ac75c5af-86e8-4282-9a8e-8db3c22cbda0">WOW64</a>, <b>IsWow64Process2</b> returns the following information:

<ul>
<li>Whether the target process, specified by <i>hProcess</i>, is running under Wow or not.</li>
<li>The architecture of the target process.</li>
<li> Optionally, the architecture of the host system.</li>
</ul>


