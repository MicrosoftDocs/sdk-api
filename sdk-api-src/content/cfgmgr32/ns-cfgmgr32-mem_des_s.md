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

# Mem_Des_s structure


## -description


The MEM_DES structure is used for specifying either a resource list or a resource requirements list that describes memory usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff547012">Hardware Resources</a>.


## -struct-fields




### -field MD_Count





#### For a resource list:

Zero.



#### For a resource requirements list:

The number of elements in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548722">MEM_RANGE</a> array that is included in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548724">MEM_RESOURCE</a> structure.


### -field MD_Type

Must be set to the constant value <b>MType_Range</b>.


### -field MD_Alloc_Base





#### For a resource list:

The lowest-numbered of a range of contiguous physical memory addresses allocated to the device.



#### For a resource requirements list:

Zero.


### -field MD_Alloc_End





#### For a resource list:

The highest-numbered of a range of contiguous physical memory addresses allocated to the device.



#### For a resource requirements list:

Zero.


### -field MD_Flags

One bit flag from <i>each</i> of the flag sets described in the following table.

<table>
<tr>
<th></th>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td colspan="2">
<i>Read-Only Flags</i>

</td>
<td></td>
</tr>
<tr>
<td></td>
<td>
<b>fMD_ROM</b>

</td>
<td>
The specified memory range is read-only.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fMD_RAM</b>

</td>
<td>
The specified memory range is not read-only.

</td>
</tr>
<tr>
<td></td>
<td>
<b>mMD_MemoryType</b>

</td>
<td>
Bitmask for the bit within <b>MD_Flags</b> that specifies the read-only attribute.

</td>
</tr>
<tr>
<td colspan="2">
<i>Write-Only Flags</i>

</td>
<td></td>
</tr>
<tr>
<td></td>
<td>
<b>fMD_ReadDisallowed</b>

</td>
<td>
The specified memory range is write-only.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fMD_ReadAllowed</b>

</td>
<td>
The specified memory range is not write-only.

</td>
</tr>
<tr>
<td></td>
<td>
<b>mMD_Readable</b>

</td>
<td>
Bitmask for the bit within <b>MD_Flags</b> that specifies the write-only attribute.

</td>
</tr>
<tr>
<td colspan="2">
<i>Address Size Flags</i>

</td>
<td></td>
</tr>
<tr>
<td></td>
<td>
<b>fMD_24</b>

</td>
<td>
24-bit addressing (<i>not used</i>).

</td>
</tr>
<tr>
<td></td>
<td>
<b>fMD_32</b>

</td>
<td>
32-bit addressing.

</td>
</tr>
<tr>
<td></td>
<td>
<b>mMD_32_24</b>

</td>
<td>
Bitmask for the bit within <b>MD_Flags</b> that specifies the address size.

</td>
</tr>
<tr>
<td colspan="2">
<i>Prefetch Flags</i>

</td>
<td></td>
</tr>
<tr>
<td></td>
<td>
<b>fMD_PrefetchAllowed</b>

</td>
<td>
The specified memory range can be prefetched.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fMD_PrefetchDisallowed</b>

</td>
<td>
The specified memory range cannot be prefetched.

</td>
</tr>
<tr>
<td></td>
<td>
<b>mMD_Prefetchable</b>

</td>
<td>
Bitmask for the bit within <b>MD_Flags</b> that specifies the prefetch ability.

</td>
</tr>
<tr>
<td colspan="2">
<i>Caching Flags</i>

</td>
<td></td>
</tr>
<tr>
<td></td>
<td>
<b>fMD_Cacheable</b>

</td>
<td>
The specified memory range can be cached.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fMD_NonCacheable</b>

</td>
<td>
The specified memory range cannot be cached.

</td>
</tr>
<tr>
<td></td>
<td>
<b>mMD_Cacheable</b>

</td>
<td>
Bitmask for the bit within <b>MD_Flags</b> that specifies the caching ability.

</td>
</tr>
<tr>
<td colspan="2">
<i>Combined-Write Caching Flags</i>

</td>
<td></td>
</tr>
<tr>
<td></td>
<td>
<b>fMD_CombinedWriteAllowed</b>

</td>
<td>
Combined-write caching is allowed.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fMD_CombinedWriteDisallowed</b>

</td>
<td>
Combined-write caching is not allowed.

</td>
</tr>
<tr>
<td></td>
<td>
<b>mMD_CombinedWrite</b>

</td>
<td>
Bitmask for the bit within <b>MD_Flags</b> that specifies the combine-write caching ability.

</td>
</tr>
</table>
 


### -field MD_Reserved

<i>For internal use only.</i>


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548722">MEM_RANGE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548724">MEM_RESOURCE</a>
 

 

