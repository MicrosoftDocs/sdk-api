---
UID: NF:memoryapi.GetSystemFileCacheSize
title: GetSystemFileCacheSize function (memoryapi.h)
description: Retrieves the current size limits for the working set of the system cache.
helpviewer_keywords: ["FILE_CACHE_MAX_HARD_ENABLE","FILE_CACHE_MIN_HARD_ENABLE","GetSystemFileCacheSize","GetSystemFileCacheSize function","base.getsystemfilecachesize","winbase/GetSystemFileCacheSize"]
old-location: base\getsystemfilecachesize.htm
tech.root: base
ms.assetid: 9a82e572-eab8-4096-a3b3-706ca6eb7a52
ms.date: 12/05/2018
ms.keywords: FILE_CACHE_MAX_HARD_ENABLE, FILE_CACHE_MIN_HARD_ENABLE, GetSystemFileCacheSize, GetSystemFileCacheSize function, base.getsystemfilecachesize, winbase/GetSystemFileCacheSize
f1_keywords:
- memoryapi/GetSystemFileCacheSize
dev_langs:
- c++
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
- API-MS-Win-Core-memory-l1-1-1.dll
- KernelBase.dll
- API-MS-Win-Core-memory-l1-1-2.dll
- API-MS-Win-Core-memory-l1-1-3.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
- API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
- GetSystemFileCacheSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetSystemFileCacheSize function


## -description


Retrieves the current size limits for the working set of the system cache.


## -parameters




### -param lpMinimumFileCacheSize [out]

A pointer to a variable that receives the minimum size of the file cache, in bytes. The virtual memory manager attempts to keep at least this much memory resident in the system file cache, if there is a previous call to the <a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-setsystemfilecachesize">SetSystemFileCacheSize</a> function with the <b>FILE_CACHE_MIN_HARD_ENABLE</b> flag.


### -param lpMaximumFileCacheSize [out]

A pointer to a variable that receives the maximum size of the file cache, in bytes. The virtual memory manager enforces this limit only if there is a previous call to <a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-setsystemfilecachesize">SetSystemFileCacheSize</a> with the <b>FILE_CACHE_MAX_HARD_ENABLE</b> flag.


### -param lpFlags [out]

The flags that indicate which of the file cache limits are enabled.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_CACHE_MAX_HARD_ENABLE"></a><a id="file_cache_max_hard_enable"></a><dl>
<dt><b>FILE_CACHE_MAX_HARD_ENABLE</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The maximum size limit is enabled. If this flag is not present, this limit is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_CACHE_MIN_HARD_ENABLE"></a><a id="file_cache_min_hard_enable"></a><dl>
<dt><b>FILE_CACHE_MIN_HARD_ENABLE</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
The minimum size limit is enabled. If this flag is not present, this limit is disabled.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is 0 (zero). To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0502 or later. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

The <b>FILE_CACHE</b> constants will be defined in the Windows header files starting with the Windows SDK for Windows Server 2008. If you are using header files from an earlier version of the SDK, add the definitions shown in <a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-setsystemfilecachesize">SetSystemFileCacheSize</a> to your code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Memory/memory-management-functions">Memory
    Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/memoryapi/nf-memoryapi-setsystemfilecachesize">SetSystemFileCacheSize</a>
 

 

