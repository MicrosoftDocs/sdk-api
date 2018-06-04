---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tagHEAPENTRY32 structure


## -description


Describes one entry (block) of a heap that is being examined.


## -struct-fields




### -field dwSize

The size of the structure, in bytes. Before calling the 
<a href="https://msdn.microsoft.com/79d01e3a-b11b-46b5-99d0-b445000288a7">Heap32First</a> function, set this member to <code>sizeof(HEAPENTRY32)</code>. If you do not initialize <b>dwSize</b>, 
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




<a href="https://msdn.microsoft.com/79d01e3a-b11b-46b5-99d0-b445000288a7">Heap32First</a>



<a href="https://msdn.microsoft.com/cc3becd0-edba-47cf-ac2d-26a5d98390e7">Heap32Next</a>
 

 

