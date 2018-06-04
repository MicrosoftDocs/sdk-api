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

# tagHEAPLIST32 structure


## -description


Describes an entry from a list that enumerates the heaps used by a specified process.


## -struct-fields




### -field dwSize

The size of the structure, in bytes. Before calling the 
<a href="https://msdn.microsoft.com/b9a2992b-0dc1-41c3-aa23-796def674831">Heap32ListFirst</a> function, set this member to <code>sizeof(HEAPLIST32)</code>. If you do not initialize <b>dwSize</b>, 
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




<a href="https://msdn.microsoft.com/b9a2992b-0dc1-41c3-aa23-796def674831">Heap32ListFirst</a>



<a href="https://msdn.microsoft.com/bb4d573c-a82f-48ac-be22-440d6a1d0c9c">Heap32ListNext</a>
 

 

