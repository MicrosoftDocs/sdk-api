---
UID: NF:memoryapi.SetSystemFileCacheSize
title: SetSystemFileCacheSize function
author: windows-sdk-content
description: Limits the size of the working set for the file system cache.
old-location: base\setsystemfilecachesize.htm
tech.root: memory
ms.assetid: bb0a65d6-d04a-4805-80d5-61fc53eb2726
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: FILE_CACHE_MAX_HARD_DISABLE, FILE_CACHE_MAX_HARD_ENABLE, FILE_CACHE_MIN_HARD_DISABLE, FILE_CACHE_MIN_HARD_ENABLE, SetSystemFileCacheSize, SetSystemFileCacheSize function, base.setsystemfilecachesize, winbase/SetSystemFileCacheSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - SetSystemFileCacheSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SetSystemFileCacheSize
: 
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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The calling process must enable the <b>SE_INCREASE_QUOTA_NAME</b> privilege.

Setting the <i>MaximumFileCacheSize</i> parameter to a very low value can adversely affect system performance.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0502 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.

The <b>FILE_CACHE_*</b> constants will be defined in the Windows header files starting with the Windows SDK for Windows Server 2008. If you are using header files from an earlier version of the SDK, add the following definitions to your code.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef FILE_CACHE_FLAGS_DEFINED

#define FILE_CACHE_MAX_HARD_ENABLE      0x00000001
#define FILE_CACHE_MAX_HARD_DISABLE     0x00000002
#define FILE_CACHE_MIN_HARD_ENABLE      0x00000004
#define FILE_CACHE_MIN_HARD_DISABLE     0x00000008

#endif // FILE_CACHE_FLAGS_DEFINED
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9a82e572-eab8-4096-a3b3-706ca6eb7a52">GetSystemFileCacheSize</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>
 

 

