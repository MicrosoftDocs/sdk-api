---
UID: NS:tlhelp32.tagHEAPENTRY32
title: HEAPENTRY32 (tlhelp32.h)
author: windows-sdk-content
description: Describes one entry (block) of a heap that is being examined.
old-location: toolhelp\heapentry32_str.htm
tech.root: ToolHelp
ms.assetid: c5f1dc66-d44f-4491-b0b7-961b163d0f1f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPHEAPENTRY32, *PHEAPENTRY32, HEAPENTRY32, HEAPENTRY32 structure [ToolHelp], LF32_FIXED, LF32_FREE, LF32_MOVEABLE, PHEAPENTRY32, PHEAPENTRY32 structure pointer [ToolHelp], _win32_heapentry32_str, base.heapentry32_str, tlhelp32/HEAPENTRY32, tlhelp32/PHEAPENTRY32, toolhelp.heapentry32_str"
ms.topic: struct
f1_keywords: ["tlhelp32/HEAPENTRY32"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - TlHelp32.h
api_name:
 - HEAPENTRY32
product: Windows
targetos: Windows
req.typenames: HEAPENTRY32
req.redist: 
ms.custom: 19H1
---

# HEAPENTRY32 structure


## -description


Describes one entry (block) of a heap that is being examined.


## -struct-fields




### -field dwSize

The size of the structure, in bytes. Before calling the 
<a href="https://docs.microsoft.com/windows/desktop/api/tlhelp32/nf-tlhelp32-heap32first">Heap32First</a> function, set this member to <code>sizeof(HEAPENTRY32)</code>. If you do not initialize <b>dwSize</b>, 
<b>Heap32First</b> fails.


### -field hHandle

A handle to the heap block.


### -field dwAddress

The linear address of the start of the block.


### -field dwBlockSize

The size of the heap block, in bytes.


### -field dwFlags

This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LF32_FIXED"></a><a id="lf32_fixed"></a><dl>
<dt><b>LF32_FIXED</b></dt>
</dl>
</td>
<td width="60%">
The memory block has a fixed (unmovable) location.

</td>
</tr>
<tr>
<td width="40%"><a id="LF32_FREE"></a><a id="lf32_free"></a><dl>
<dt><b>LF32_FREE</b></dt>
</dl>
</td>
<td width="60%">
The memory block is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="LF32_MOVEABLE"></a><a id="lf32_moveable"></a><dl>
<dt><b>LF32_MOVEABLE</b></dt>
</dl>
</td>
<td width="60%">
The memory block location can be moved.

</td>
</tr>
</table>
 


### -field dwLockCount

This member is no longer used and is always set to zero.


### -field dwResvd

Reserved; do not use or alter.


### -field th32ProcessID

The identifier of the process that uses the heap.


### -field th32HeapID

The heap identifier. This is not a handle, and has meaning only to the tool help functions.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tlhelp32/nf-tlhelp32-heap32first">Heap32First</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tlhelp32/nf-tlhelp32-heap32next">Heap32Next</a>
 

 

