---
UID: NF:tlhelp32.Heap32ListNext
title: Heap32ListNext function (tlhelp32.h)
description: Retrieves information about the next heap that has been allocated by a process.
helpviewer_keywords: ["Heap32ListNext","Heap32ListNext function [ToolHelp]","_win32_heap32listnext","base.heap32listnext","tlhelp32/Heap32ListNext","toolhelp.heap32listnext"]
old-location: toolhelp\heap32listnext.htm
tech.root: ToolHelp
ms.assetid: bb4d573c-a82f-48ac-be22-440d6a1d0c9c
ms.date: 12/05/2018
ms.keywords: Heap32ListNext, Heap32ListNext function [ToolHelp], _win32_heap32listnext, base.heap32listnext, tlhelp32/Heap32ListNext, toolhelp.heap32listnext
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
 - Heap32ListNext
 - tlhelp32/Heap32ListNext
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
 - Heap32ListNext
---

# Heap32ListNext function


## -description

Retrieves information about the next heap that has been allocated by a process.

## -parameters

### -param hSnapshot [in]

A handle to the snapshot returned from a previous call to the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a> function.

### -param lphl [out]

A pointer to a 
<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-heaplist32">HEAPLIST32</a> structure.

## -returns

Returns <b>TRUE</b> if the next entry of the heap list has been copied to the buffer or <b>FALSE</b> otherwise. The <b>ERROR_NO_MORE_FILES</b> error value is returned by the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function when no more entries in the heap list exist.

## -remarks

To retrieve information about the first heap in a heap list, use the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-heap32listfirst">Heap32ListFirst</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/ToolHelp/traversing-the-heap-list">Traversing the Heap List</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a>



<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-heaplist32">HEAPLIST32</a>



<a href="/windows/desktop/ToolHelp/heap-lists-and-heap-walking">Heap Lists and Heap Walking</a>



<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-heap32listfirst">Heap32ListFirst</a>



<a href="/windows/desktop/ToolHelp/tool-help-functions">Tool Help Functions</a>