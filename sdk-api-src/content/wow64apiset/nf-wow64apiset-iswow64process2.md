---
UID: NF:wow64apiset.IsWow64Process2
title: IsWow64Process2 function
author: windows-sdk-content
description: Determines whether the specified process is running under WOW64; also returns additional machine process and architecture information.
old-location: base\iswow64process2.htm
tech.root: procthread
ms.assetid: 77B4E3C8-F9DE-4674-9CEA-9C81AEEB393C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IsWow64Process2, IsWow64Process2 function, base.iswow64process2, wow64apiset/IsWow64Process2
ms.topic: function
req.header: wow64apiset.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1511 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-misc-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Wow64-l1-1-0.dll
 - API-MS-Win-Core-Wow64-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - bcrypt.dll
api_name:
 - IsWow64Process2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


