---
UID: NF:tlhelp32.Heap32First
title: Heap32First function (tlhelp32.h)
description: Retrieves information about the first block of a heap that has been allocated by a process.
helpviewer_keywords: ["Heap32First","Heap32First function [ToolHelp]","_win32_heap32first","base.heap32first","tlhelp32/Heap32First","toolhelp.heap32first"]
old-location: toolhelp\heap32first.htm
tech.root: ToolHelp
ms.assetid: 79d01e3a-b11b-46b5-99d0-b445000288a7
ms.date: 12/05/2018
ms.keywords: Heap32First, Heap32First function [ToolHelp], _win32_heap32first, base.heap32first, tlhelp32/Heap32First, toolhelp.heap32first
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
 - Heap32First
 - tlhelp32/Heap32First
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
 - Heap32First
---

# Heap32First function


## -description

Retrieves information about the first block of a heap that has been allocated by a process.

## -parameters

### -param lphe [in, out]

A pointer to a 
<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-heapentry32">HEAPENTRY32</a> structure.

### -param th32ProcessID [in]

The identifier of the process context that owns the heap.

### -param th32HeapID [in]

The identifier of the heap to be enumerated.

## -returns

Returns <b>TRUE</b> if information for the first heap block has been copied to the buffer or <b>FALSE</b> otherwise. The <b>ERROR_NO_MORE_FILES</b> error value is returned by the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function if the heap is invalid or empty.

## -remarks

The calling application must set the <b>dwSize</b> member of 
<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-heapentry32">HEAPENTRY32</a> to the size, in bytes, of the structure. 
<b>Heap32First</b> changes <b>dwSize</b> to the number of bytes written to the structure. This will never be greater than the initial value of <b>dwSize</b>, but it may be smaller. If the value is smaller, do not rely on the values of any members whose offsets are greater than this value.

To access subsequent blocks of the same heap, use the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-heap32next">Heap32Next</a> function.

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



<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-heap32next">Heap32Next</a>



<a href="/windows/desktop/ToolHelp/tool-help-functions">Tool Help Functions</a>