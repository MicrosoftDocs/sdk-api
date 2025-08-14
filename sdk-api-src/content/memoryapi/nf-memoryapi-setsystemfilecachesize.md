---
UID: NF:memoryapi.SetSystemFileCacheSize
title: SetSystemFileCacheSize function (memoryapi.h)
description: Limits the size of the working set for the file system cache.
helpviewer_keywords: ["FILE_CACHE_MAX_HARD_DISABLE","FILE_CACHE_MAX_HARD_ENABLE","FILE_CACHE_MIN_HARD_DISABLE","FILE_CACHE_MIN_HARD_ENABLE","SetSystemFileCacheSize","SetSystemFileCacheSize function","base.setsystemfilecachesize","winbase/SetSystemFileCacheSize"]
old-location: base\setsystemfilecachesize.htm
tech.root: base
ms.assetid: bb0a65d6-d04a-4805-80d5-61fc53eb2726
ms.date: 12/05/2018
ms.keywords: FILE_CACHE_MAX_HARD_DISABLE, FILE_CACHE_MAX_HARD_ENABLE, FILE_CACHE_MIN_HARD_DISABLE, FILE_CACHE_MIN_HARD_ENABLE, SetSystemFileCacheSize, SetSystemFileCacheSize function, base.setsystemfilecachesize, winbase/SetSystemFileCacheSize
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
req.lib: onecore.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetSystemFileCacheSize
 - memoryapi/SetSystemFileCacheSize
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
 - API-MS-Win-Core-memory-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - SetSystemFileCacheSize
---

# SetSystemFileCacheSize function


## -description

Limits the size of the working set for the file system cache.

## -parameters

### -param MinimumFileCacheSize [in]

The minimum size of the file cache, in bytes. The virtual memory manager attempts to keep at least this much memory resident in the system file cache.

To flush the cache, specify <code>(SIZE_T) -1</code>.

### -param MaximumFileCacheSize [in]

The maximum size of the file cache, in bytes. The virtual memory manager enforces this limit only if this call or a previous call to <b>SetSystemFileCacheSize</b> specifies <b>FILE_CACHE_MAX_HARD_ENABLE</b>.

To flush the cache, specify <code>(SIZE_T) -1</code>.

### -param Flags [in]

The flags that enable or disable the file cache limits. If this parameter is 0 (zero), the size limits retain the current setting, which is either disabled or enabled.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_CACHE_MAX_HARD_DISABLE"></a><a id="file_cache_max_hard_disable"></a><dl>
<dt><b>FILE_CACHE_MAX_HARD_DISABLE</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Disable the maximum size limit.

The <b>FILE_CACHE_MAX_HARD_DISABLE</b> and <b>FILE_CACHE_MAX_HARD_ENABLE</b> flags are mutually exclusive.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_CACHE_MAX_HARD_ENABLE"></a><a id="file_cache_max_hard_enable"></a><dl>
<dt><b>FILE_CACHE_MAX_HARD_ENABLE</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Enable the maximum size limit.

The <b>FILE_CACHE_MAX_HARD_DISABLE</b> and <b>FILE_CACHE_MAX_HARD_ENABLE</b> flags are mutually exclusive.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_CACHE_MIN_HARD_DISABLE"></a><a id="file_cache_min_hard_disable"></a><dl>
<dt><b>FILE_CACHE_MIN_HARD_DISABLE</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
Disable the minimum size limit.

The <b>FILE_CACHE_MIN_HARD_DISABLE</b> and <b>FILE_CACHE_MIN_HARD_ENABLE</b> flags are mutually exclusive.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_CACHE_MIN_HARD_ENABLE"></a><a id="file_cache_min_hard_enable"></a><dl>
<dt><b>FILE_CACHE_MIN_HARD_ENABLE</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
Enable the minimum size limit.

The <b>FILE_CACHE_MIN_HARD_DISABLE</b> and <b>FILE_CACHE_MIN_HARD_ENABLE</b> flags are mutually exclusive.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is 0 (zero). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The calling process must enable the <b>SE_INCREASE_QUOTA_NAME</b> privilege.

Setting the <i>MaximumFileCacheSize</i> parameter to a very low value can adversely affect system performance.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0502 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

The <b>FILE_CACHE_*</b> constants will be defined in the Windows header files starting with the Windows SDK for Windows Server 2008. If you are using header files from an earlier version of the SDK, add the following definitions to your code.


```cpp
#ifndef FILE_CACHE_FLAGS_DEFINED

#define FILE_CACHE_MAX_HARD_ENABLE      0x00000001
#define FILE_CACHE_MAX_HARD_DISABLE     0x00000002
#define FILE_CACHE_MIN_HARD_ENABLE      0x00000004
#define FILE_CACHE_MIN_HARD_DISABLE     0x00000008

#endif // FILE_CACHE_FLAGS_DEFINED

```

## -see-also

<a href="/windows/desktop/api/memoryapi/nf-memoryapi-getsystemfilecachesize">GetSystemFileCacheSize</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>