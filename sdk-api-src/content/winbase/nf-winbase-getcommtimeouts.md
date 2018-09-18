---
UID: NF:winbase.GetCommTimeouts
title: GetCommTimeouts function
author: windows-sdk-content
description: Retrieves the time-out parameters for all read and write operations on a specified communications device.
old-location: base\getcommtimeouts.htm
tech.root: devio
ms.assetid: a5375b2e-0992-4e47-a20f-8a793addeef6
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: GetCommTimeouts, GetCommTimeouts function, _win32_getcommtimeouts, base.getcommtimeouts, winbase/GetCommTimeouts
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-comm-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetCommTimeouts
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetCommTimeouts function


## -description


Retrieves the time-out parameters for all read and write operations on a specified communications device.


## -parameters




### -param hFile [in]

A handle to the communications device. The 
<a href="base.createfile">CreateFile</a> function returns this handle.


### -param lpCommTimeouts [out]

A pointer to a 
<a href="https://msdn.microsoft.com/259aa110-b2c3-4583-a3f9-805a42025a81">COMMTIMEOUTS</a> structure in which the time-out information is returned.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



For more information about time-out values for communications devices, see the 
<a href="https://msdn.microsoft.com/71aa6ab3-d56c-43bc-9932-5b4e61fc4b30">SetCommTimeouts</a>function.




## -see-also




<a href="https://msdn.microsoft.com/259aa110-b2c3-4583-a3f9-805a42025a81">COMMTIMEOUTS</a>



<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>



<a href="base.createfile">CreateFile</a>



<a href="https://msdn.microsoft.com/71aa6ab3-d56c-43bc-9932-5b4e61fc4b30">SetCommTimeouts</a>
 

 

