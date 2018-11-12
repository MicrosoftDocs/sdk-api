---
UID: NF:sysinfoapi.GetTickCount64
title: GetTickCount64 function
author: windows-sdk-content
description: Retrieves the number of milliseconds that have elapsed since the system was started.
old-location: base\gettickcount64.htm
tech.root: sysinfo
ms.assetid: 3ebf05b9-cc53-43ae-bbcb-7841793a9d84
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetTickCount64, GetTickCount64 function, base.gettickcount64, sysinfoapi/GetTickCount64
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-SysInfo-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - GetTickCount64
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetTickCount64 function


## -description


Retrieves the number of milliseconds that have elapsed since the system was started.


## -parameters






## -returns



The number of milliseconds.




## -remarks



The resolution of the <b>GetTickCount64</b> function is limited to the resolution of the system timer, which is typically in the range of  10 milliseconds to 16 milliseconds. The resolution of the <b>GetTickCount64</b> function is not affected by adjustments made by the 
<a href="https://msdn.microsoft.com/6c748726-c81d-4669-87a1-28aad0fccead">GetSystemTimeAdjustment</a> function.

If you need a higher resolution timer, use a 
<a href="https://msdn.microsoft.com/25e0b313-64ff-4f30-ae0a-ac364ce3f0cf">multimedia timer</a> or a 
<a href="_win32_about_timers_cpp">high-resolution timer</a>.

To obtain the time the system has spent in the working state since it was started, use the <a href="https://msdn.microsoft.com/f9cf5440-9be9-4ff9-b85c-2779b847954c">QueryUnbiasedInterruptTime</a> function. 

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/f9cf5440-9be9-4ff9-b85c-2779b847954c">QueryUnbiasedInterruptTime</a> function produces different results on debug ("checked") builds of Windows, because the interrupt-time count and tick count are advanced by approximately 49 days. This helps to identify bugs that might not occur until the system has been running for a long time. The checked build is available to MSDN subscribers through the <a href="http://msdn.microsoft.com/en-us/default.aspx">Microsoft Developer Network (MSDN)</a> Web site.</div>
<div> </div>
To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>



<a href="https://msdn.microsoft.com/95c00204-bfdf-4376-9aae-8d8139ba6750">Windows Time</a>
 

 

