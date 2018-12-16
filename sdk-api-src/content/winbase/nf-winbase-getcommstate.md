---
UID: NF:winbase.GetCommState
title: GetCommState function
author: windows-sdk-content
description: Retrieves the current control settings for a specified communications device.
old-location: base\getcommstate.htm
tech.root: devio
ms.assetid: 974c2ddc-9f7f-445e-ac47-8cd86817ce9b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCommState, GetCommState function, _win32_getcommstate, base.getcommstate, winbase/GetCommState
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
 - GetCommState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetCommState function


## -description


Retrieves the current control settings for a specified communications device.


## -parameters




### -param hFile [in]

A handle to the communications device. The 
<a href="https://msdn.microsoft.com/en-us/library/Aa363858(v=VS.85).aspx">CreateFile</a> function returns this handle.


### -param lpDCB [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/9dccd2c6-44b7-4609-a2b9-9815430bf3c7">DCB</a> structure that receives the control settings information.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363858(v=VS.85).aspx">CreateFile</a>



<a href="https://msdn.microsoft.com/9dccd2c6-44b7-4609-a2b9-9815430bf3c7">DCB</a>



<a href="https://msdn.microsoft.com/a9296514-4789-4830-ba68-84a16ac7fc47">SetCommState</a>
 

 

