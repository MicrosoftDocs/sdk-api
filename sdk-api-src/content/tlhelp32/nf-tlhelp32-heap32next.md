---
UID: NF:tlhelp32.Heap32Next
title: Heap32Next function (tlhelp32.h)
description: Retrieves information about the next block of a heap that has been allocated by a process.
helpviewer_keywords: ["Heap32Next","Heap32Next function [ToolHelp]","_win32_heap32next","base.heap32next","tlhelp32/Heap32Next","toolhelp.heap32next"]
old-location: toolhelp\heap32next.htm
tech.root: ToolHelp
ms.assetid: cc3becd0-edba-47cf-ac2d-26a5d98390e7
ms.date: 12/05/2018
ms.keywords: Heap32Next, Heap32Next function [ToolHelp], _win32_heap32next, base.heap32next, tlhelp32/Heap32Next, toolhelp.heap32next
req.header: tlhelp32.h
req.include-header: 
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
 - Heap32Next
 - tlhelp32/Heap32Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ToolHelp-L1-1-1.dll
 - Kernel32Legacy.dll
api_name:
 - Heap32Next
---

# Heap32Next function


## -description

Retrieves information about the next block of a heap that has been allocated by a process.

## -parameters

### -param lphe [out]

A pointer to a 
<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-heapentry32">HEAPENTRY32</a> structure.

## -returns

Returns <b>TRUE</b> if information about the next block in the heap has been copied to the buffer or <b>FALSE</b> otherwise. The 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns <b>ERROR_NO_MORE_FILES</b> when no more objects in the heap exist and <b>ERROR_INVALID_DATA</b> if the heap appears to be corrupt or is modified during the walk in such a way that 
<b>Heap32Next</b> cannot continue.

## -remarks

To retrieve information for the first block of a heap, use the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-heap32first">Heap32First</a> function.

The <b>Heap32Next</b> function does not maintain a reference to the target process. If the target process dies, the system may create a new process using the same process identifier. Therefore, the caller should maintain a reference to the target process as long as it is using <b>Heap32Next</b>.

Walking the heap with <b>Heap32First</b> and <b>Heap32Next</b> is inefficient, particularly for large heaps.
Use
<a href="/windows/desktop/api/heapapi/nf-heapapi-heapwalk">HeapWalk</a> instead.

#### Examples

For an example, see 
<a href="/windows/desktop/ToolHelp/traversing-the-heap-list">Traversing the Heap List</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-heapentry32">HEAPENTRY32</a>



<a href="/windows/desktop/ToolHelp/heap-lists-and-heap-walking">Heap Lists and Heap Walking</a>



<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-heap32first">Heap32First</a>



<a href="/windows/desktop/ToolHelp/tool-help-functions">Tool Help Functions</a>