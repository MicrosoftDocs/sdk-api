---
UID: NF:tlhelp32.Heap32ListFirst
title: Heap32ListFirst function (tlhelp32.h)
description: Retrieves information about the first heap that has been allocated by a specified process.
helpviewer_keywords: ["Heap32ListFirst","Heap32ListFirst function [ToolHelp]","_win32_heap32listfirst","base.heap32listfirst","tlhelp32/Heap32ListFirst","toolhelp.heap32listfirst"]
old-location: toolhelp\heap32listfirst.htm
tech.root: ToolHelp
ms.assetid: b9a2992b-0dc1-41c3-aa23-796def674831
ms.date: 12/05/2018
ms.keywords: Heap32ListFirst, Heap32ListFirst function [ToolHelp], _win32_heap32listfirst, base.heap32listfirst, tlhelp32/Heap32ListFirst, toolhelp.heap32listfirst
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
 - Heap32ListFirst
 - tlhelp32/Heap32ListFirst
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
 - Heap32ListFirst
---

# Heap32ListFirst function


## -description

Retrieves information about the first heap that has been allocated by a specified process.

## -parameters

### -param hSnapshot [in]

A handle to the snapshot returned from a previous call to the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a> function.

### -param lphl [in, out]

A pointer to a 
<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-heaplist32">HEAPLIST32</a> structure.

## -returns

Returns <b>TRUE</b> if the first entry of the heap list has been copied to the buffer or <b>FALSE</b> otherwise. The <b>ERROR_NO_MORE_FILES</b> error value is returned by the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function when no heap list exists or the snapshot does not contain heap list information.

## -remarks

The calling application must set the <b>dwSize</b> member of 
<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-heapentry32">HEAPLIST32</a> to the size, in bytes, of the structure. 
<b>Heap32ListFirst</b> changes <b>dwSize</b> to the number of bytes written to the structure. This will never be greater than the initial value of <b>dwSize</b>, but it may be smaller. If the value is smaller, do not rely on the values of any members whose offsets are greater than this value.

To retrieve information about other heaps in the heap list, use the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-heap32listnext">Heap32ListNext</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/ToolHelp/traversing-the-heap-list">Traversing the Heap List</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a>



<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-heaplist32">HEAPLIST32</a>



<a href="/windows/desktop/ToolHelp/heap-lists-and-heap-walking">Heap Lists and Heap Walking</a>



<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-heap32listnext">Heap32ListNext</a>



<a href="/windows/desktop/ToolHelp/tool-help-functions">Tool Help Functions</a>