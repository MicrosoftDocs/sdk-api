---
UID: NF:winbase.ClearCommBreak
title: ClearCommBreak function
author: windows-sdk-content
description: Restores character transmission for a specified communications device and places the transmission line in a nonbreak state.
old-location: base\clearcommbreak.htm
tech.root: devio
ms.assetid: 9692242c-e209-4492-ab0b-333f09595597
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ClearCommBreak, ClearCommBreak function, _win32_clearcommbreak, base.clearcommbreak, winbase/ClearCommBreak
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
 - ClearCommBreak
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClearCommBreak function


## -description


Restores character transmission for a specified communications device and places the transmission line in a nonbreak state.


## -parameters




### -param hFile [in]

A handle to the communications device. The 
<a href="https://msdn.microsoft.com/en-us/library/Aa363858(v=VS.85).aspx">CreateFile</a> function returns this handle.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A communications device is placed in a break state by the 
<a href="https://msdn.microsoft.com/997fa1e0-c585-4517-abe7-77b9b08440ee">SetCommBreak</a> or 
<a href="https://msdn.microsoft.com/27c4ebdf-1c06-4a60-8e49-dcccba10789c">EscapeCommFunction</a> function. Character transmission is then suspended until the break state is cleared by calling 
<b>ClearCommBreak</b>.




## -see-also




<a href="https://msdn.microsoft.com/9cc52104-aa5e-4baa-86f1-8c6dcdd661ef">ClearCommError</a>



<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363858(v=VS.85).aspx">CreateFile</a>



<a href="https://msdn.microsoft.com/27c4ebdf-1c06-4a60-8e49-dcccba10789c">EscapeCommFunction</a>



<a href="https://msdn.microsoft.com/997fa1e0-c585-4517-abe7-77b9b08440ee">SetCommBreak</a>
 

 

