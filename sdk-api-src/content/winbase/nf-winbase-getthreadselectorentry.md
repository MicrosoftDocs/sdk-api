---
UID: NF:winbase.GetThreadSelectorEntry
title: GetThreadSelectorEntry function (winbase.h)
description: Retrieves a descriptor table entry for the specified selector and thread.
helpviewer_keywords: ["GetThreadSelectorEntry","GetThreadSelectorEntry function","_win32_getthreadselectorentry","base.getthreadselectorentry","winbase/GetThreadSelectorEntry"]
old-location: base\getthreadselectorentry.htm
tech.root: Debug
ms.assetid: 9bf6f7b1-7a30-4398-a12a-b1de986f860d
ms.date: 12/05/2018
ms.keywords: GetThreadSelectorEntry, GetThreadSelectorEntry function, _win32_getthreadselectorentry, base.getthreadselectorentry, winbase/GetThreadSelectorEntry
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetThreadSelectorEntry
 - winbase/GetThreadSelectorEntry
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetThreadSelectorEntry
---

# GetThreadSelectorEntry function


## -description

Retrieves a descriptor table entry for the specified selector and thread.

## -parameters

### -param hThread [in]

A handle to the thread containing the specified selector. The handle must have THREAD_QUERY_INFORMATION access. For more information, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

### -param dwSelector [in]

The global or local selector value to look up in the thread's descriptor tables.

### -param lpSelectorEntry [out]

A pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-ldt_entry">LDT_ENTRY</a> structure that receives a copy of the descriptor table entry if the specified selector has an entry in the specified thread's descriptor table. This information can be used to convert a segment-relative address to a linear virtual address.

## -returns

If the function succeeds, the return value is nonzero. In that case, the structure pointed to by the <i>lpSelectorEntry</i> parameter receives a copy of the specified descriptor table entry.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>GetThreadSelectorEntry</b> is only functional on x86-based systems. For systems that are not x86-based, the function returns <b>FALSE</b>.

Debuggers use this function to convert segment-relative addresses to linear virtual addresses. The 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-readprocessmemory">ReadProcessMemory</a> and 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-writeprocessmemory">WriteProcessMemory</a> functions use linear virtual addresses.

## -see-also

<a href="/windows/desktop/Debug/debugging-functions">Debugging Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-ldt_entry">LDT_ENTRY</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-readprocessmemory">ReadProcessMemory</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-writeprocessmemory">WriteProcessMemory</a>