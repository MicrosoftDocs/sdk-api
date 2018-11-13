---
UID: NF:sysinfoapi.GetLocalTime
title: GetLocalTime function
author: windows-sdk-content
description: Retrieves the current local date and time.
old-location: base\getlocaltime.htm
tech.root: SysInfo
ms.assetid: a63fcd36-de48-4437-a823-837884cc2bf9
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: GetLocalTime, GetLocalTime function, _win32_getlocaltime, base.getlocaltime, sysinfoapi/GetLocalTime
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
 - GetLocalTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetLocalTime function


## -description


Retrieves the current local date and time.

To retrieve the current date and time in Coordinated Universal Time (UTC) format, use the <a href="https://msdn.microsoft.com/9ed8386b-f035-446f-b0f8-12e0d3f23aac">GetSystemTime</a> function.


## -parameters




### -param lpSystemTime [out]

A pointer to a 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure to receive the current local date and time.


## -returns



This function does not return a value.




## -remarks



To set the current local date and time, use the <a href="https://msdn.microsoft.com/c2d2bac7-4171-4b8b-81e8-0e8a1b2794e6">SetLocalTime</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9ed8386b-f035-446f-b0f8-12e0d3f23aac">GetSystemTime</a>



<a href="https://msdn.microsoft.com/a6570ec5-ac77-427a-86d9-32cbecc62e37">Local Time</a>



<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>



<a href="https://msdn.microsoft.com/c2d2bac7-4171-4b8b-81e8-0e8a1b2794e6">SetLocalTime</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

