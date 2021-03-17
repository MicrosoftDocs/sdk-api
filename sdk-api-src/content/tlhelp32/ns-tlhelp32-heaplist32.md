---
UID: NS:tlhelp32.tagHEAPLIST32
title: HEAPLIST32 (tlhelp32.h)
description: Describes an entry from a list that enumerates the heaps used by a specified process.
helpviewer_keywords: ["*LPHEAPLIST32","*PHEAPLIST32","HEAPLIST32","HEAPLIST32 structure [ToolHelp]","HF32_DEFAULT","PHEAPLIST32","PHEAPLIST32 structure pointer [ToolHelp]","_win32_heaplist32_str","base.heaplist32_str","tlhelp32/HEAPLIST32","tlhelp32/PHEAPLIST32","toolhelp.heaplist32_str"]
old-location: toolhelp\heaplist32_str.htm
tech.root: ToolHelp
ms.assetid: 61e01d23-9f15-44c5-9f6d-45df4809ccad
ms.date: 12/05/2018
ms.keywords: '*LPHEAPLIST32, *PHEAPLIST32, HEAPLIST32, HEAPLIST32 structure [ToolHelp], HF32_DEFAULT, PHEAPLIST32, PHEAPLIST32 structure pointer [ToolHelp], _win32_heaplist32_str, base.heaplist32_str, tlhelp32/HEAPLIST32, tlhelp32/PHEAPLIST32, toolhelp.heaplist32_str'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: HEAPLIST32
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHEAPLIST32
 - tlhelp32/tagHEAPLIST32
 - HEAPLIST32
 - tlhelp32/HEAPLIST32
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - TlHelp32.h
api_name:
 - HEAPLIST32
---

# HEAPLIST32 structure


## -description

Describes an entry from a list that enumerates the heaps used by a specified process.

## -struct-fields

### -field dwSize

The size of the structure, in bytes. Before calling the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-heap32listfirst">Heap32ListFirst</a> function, set this member to <code>sizeof(HEAPLIST32)</code>. If you do not initialize <b>dwSize</b>, 
<b>Heap32ListFirst</b> will fail.

### -field th32ProcessID

The identifier of the process to be examined.

### -field th32HeapID

The heap identifier. This is not a handle, and has meaning only to the tool help functions.

### -field dwFlags

This member can be one of the  following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HF32_DEFAULT"></a><a id="hf32_default"></a><dl>
<dt><b>HF32_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Process's default heap

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-heap32listfirst">Heap32ListFirst</a>



<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-heap32listnext">Heap32ListNext</a>