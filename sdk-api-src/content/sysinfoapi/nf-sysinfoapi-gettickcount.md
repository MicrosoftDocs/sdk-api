---
UID: NF:sysinfoapi.GetTickCount
title: GetTickCount function
author: windows-sdk-content
description: Retrieves the number of milliseconds that have elapsed since the system was started, up to 49.7 days.
old-location: base\gettickcount.htm
tech.root: sysinfo
ms.assetid: 22201c82-a49a-4972-9f49-6baf6d23a1ea
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTickCount, GetTickCount function, _win32_gettickcount, base.gettickcount, sysinfoapi/GetTickCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - GetTickCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetTickCount function


## -description


Retrieves the number of milliseconds that have elapsed since the system was started, up to 49.7 days.


## -parameters






## -returns



The return value is the number of milliseconds that have elapsed since the system was started.




## -remarks



The resolution of the <b>GetTickCount</b> function is limited to the resolution of the system timer, which is typically in the range of  10 milliseconds to 16 milliseconds. The resolution of the <b>GetTickCount</b> function is not affected by adjustments made by the 
<a href="https://msdn.microsoft.com/6c748726-c81d-4669-87a1-28aad0fccead">GetSystemTimeAdjustment</a> function.

The elapsed time is stored as a <b>DWORD</b> value. Therefore, the time will wrap around to zero if the system is run continuously for 49.7 days. To avoid this problem, use the <a href="https://msdn.microsoft.com/3ebf05b9-cc53-43ae-bbcb-7841793a9d84">GetTickCount64</a> function. Otherwise, check for an overflow condition when comparing times.

If you need a higher resolution timer, use a 
<a href="https://msdn.microsoft.com/25e0b313-64ff-4f30-ae0a-ac364ce3f0cf">multimedia timer</a> or a 
<a href="https://msdn.microsoft.com/library/ms644900(v=VS.85).aspx">high-resolution timer</a>.

To obtain the time elapsed since the computer was started, retrieve the System Up Time counter in the performance data in the registry key <b>HKEY_PERFORMANCE_DATA</b>. The value returned is an 8-byte value. For more information, see 
<a href="https://msdn.microsoft.com/9dcb7e84-a7d6-43b5-8fe9-4e33d683c74c">Performance Counters</a>. 

To obtain the time the system has spent in the working state since it was started, use the <a href="https://msdn.microsoft.com/f9cf5440-9be9-4ff9-b85c-2779b847954c">QueryUnbiasedInterruptTime</a> function.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/f9cf5440-9be9-4ff9-b85c-2779b847954c">QueryUnbiasedInterruptTime</a> function produces different results on debug ("checked") builds of Windows, because the interrupt-time count and tick count are advanced by approximately 49 days. This helps to identify bugs that might not occur until the system has been running for a long time. The checked build is available to MSDN subscribers through the <a href="http://msdn.microsoft.com/en-us/default.aspx">Microsoft Developer Network (MSDN)</a> Web site.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>



<a href="https://msdn.microsoft.com/95c00204-bfdf-4376-9aae-8d8139ba6750">Windows Time</a>
 

 

