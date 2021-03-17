---
UID: NF:winbase.Wow64GetThreadSelectorEntry
title: Wow64GetThreadSelectorEntry function (winbase.h)
description: Retrieves a descriptor table entry for the specified selector and WOW64 thread.
helpviewer_keywords: ["Wow64GetThreadSelectorEntry","Wow64GetThreadSelectorEntry function","base.wow64getthreadselectorentry","winbase/Wow64GetThreadSelectorEntry"]
old-location: base\wow64getthreadselectorentry.htm
tech.root: Debug
ms.assetid: 68393913-6725-4cc6-90b9-57da2a96c91e
ms.date: 12/05/2018
ms.keywords: Wow64GetThreadSelectorEntry, Wow64GetThreadSelectorEntry function, base.wow64getthreadselectorentry, winbase/Wow64GetThreadSelectorEntry
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Wow64GetThreadSelectorEntry
 - winbase/Wow64GetThreadSelectorEntry
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - Wow64GetThreadSelectorEntry
---

# Wow64GetThreadSelectorEntry function


## -description

Retrieves a descriptor table entry for the specified selector and WOW64 thread.

## -parameters

### -param hThread [in]

A handle to the thread containing the
        specified selector.  The handle must have been created with
        THREAD_QUERY_INFORMATION access to the thread. For more information, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

### -param dwSelector [in]

The global or local selector value to look up in the thread's descriptor tables.

### -param lpSelectorEntry [out]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-wow64_ldt_entry">WOW64_LDT_ENTRY</a> structure that receives a copy of the descriptor table entry if the specified selector has an entry in the specified thread's descriptor table. This information can be used to convert a segment-relative address to a linear virtual address.

## -returns

If the function succeeds, the return value is nonzero. In that case, the structure pointed to by the <i>lpSelectorEntry</i> parameter receives a copy of the specified descriptor table entry.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>Wow64GetThreadSelectorEntry</b> function is functional only on 64-bit systems and can be called only by 64-bit processes. If this function is called by a 32-bit process, the function fails with ERROR_NOT_SUPPORTED. A 32-bit process should use the <a href="/windows/desktop/api/winbase/nf-winbase-getthreadselectorentry">GetThreadSelectorEntry</a> function instead. 

Debuggers use this function to convert segment-relative addresses to linear virtual addresses. The 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-readprocessmemory">ReadProcessMemory</a> and 
<a href="/windows/desktop/api/memoryapi/nf-memoryapi-writeprocessmemory">WriteProcessMemory</a> functions use linear virtual addresses.