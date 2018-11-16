---
UID: NF:memoryapi.GetMemoryErrorHandlingCapabilities
title: GetMemoryErrorHandlingCapabilities function
author: windows-sdk-content
description: Gets the memory error handling capabilities of the system.
old-location: base\getmemoryerrorhandlingcapabilities.htm
tech.root: Memory
ms.assetid: 03a22996-7275-4c9b-838e-424ad92c6606
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetMemoryErrorHandlingCapabilities, GetMemoryErrorHandlingCapabilities function, MEHC_PATROL_SCRUBBER_PRESENT, base.getmemoryerrorhandlingcapabilities, winbase/GetMemoryErrorHandlingCapabilities
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - API-MS-Win-Core-memory-l1-1-2.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - GetMemoryErrorHandlingCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetMemoryErrorHandlingCapabilities
: 
---

# GetMemoryErrorHandlingCapabilities function


## -description


Gets the memory error handling capabilities of the system.


## -parameters




### -param Capabilities [out]

A <b>PULONG</b> that receives one or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MEHC_PATROL_SCRUBBER_PRESENT"></a><a id="mehc_patrol_scrubber_present"></a><dl>
<dt><b>MEHC_PATROL_SCRUBBER_PRESENT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The hardware can detect and report failed memory.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that calls this function, define <b>_WIN32_WINNT</b> as 
    <b>_WIN32_WINNT_WIN8</b> or higher. For more information, see 
    <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.



