---
UID: NF:memoryapi.GetMemoryErrorHandlingCapabilities
title: GetMemoryErrorHandlingCapabilities function (memoryapi.h)
description: Gets the memory error handling capabilities of the system.
helpviewer_keywords: ["GetMemoryErrorHandlingCapabilities","GetMemoryErrorHandlingCapabilities function","MEHC_PATROL_SCRUBBER_PRESENT","base.getmemoryerrorhandlingcapabilities","winbase/GetMemoryErrorHandlingCapabilities"]
old-location: base\getmemoryerrorhandlingcapabilities.htm
tech.root: base
ms.assetid: 03a22996-7275-4c9b-838e-424ad92c6606
ms.date: 12/05/2018
ms.keywords: GetMemoryErrorHandlingCapabilities, GetMemoryErrorHandlingCapabilities function, MEHC_PATROL_SCRUBBER_PRESENT, base.getmemoryerrorhandlingcapabilities, winbase/GetMemoryErrorHandlingCapabilities
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
req.lib: onecore.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetMemoryErrorHandlingCapabilities
 - memoryapi/GetMemoryErrorHandlingCapabilities
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-memory-l1-1-9.dll
 - api-ms-win-core-memory-l1-1-8.dll
 - api-ms-win-core-memory-l1-1-7.dll
 - api-ms-win-core-memory-l1-1-6.dll
 - api-ms-win-core-memory-l1-1-5.dll
 - Kernel32.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - GetMemoryErrorHandlingCapabilities
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
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To compile an application that calls this function, define <b>_WIN32_WINNT</b> as 
    <b>_WIN32_WINNT_WIN8</b> or higher. For more information, see 
    <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.