---
UID: NS:cfgmgr32.Mem_Des_s
title: MEM_DES (cfgmgr32.h)
description: The MEM_DES structure is used for specifying either a resource list or a resource requirements list that describes memory usage for a device instance. For more information about resource lists and resource requirements lists, see Hardware Resources.
helpviewer_keywords: ["*PMEM_DES","MEM_DES","MEM_DES structure [Device and Driver Installation]","PMEM_DES","PMEM_DES structure pointer [Device and Driver Installation]","cfgmgr32/MEM_DES","cfgmgr32/PMEM_DES","cfgmgrst_cdbb69b5-e18f-4721-bb66-c6160d959f10.xml","devinst.mem_des"]
old-location: devinst\mem_des.htm
tech.root: devinst
ms.assetid: 1a9ee8f2-fabe-4351-b11e-93f46e190d66
ms.date: 12/05/2018
ms.keywords: '*PMEM_DES, MEM_DES, MEM_DES structure [Device and Driver Installation], PMEM_DES, PMEM_DES structure pointer [Device and Driver Installation], cfgmgr32/MEM_DES, cfgmgr32/PMEM_DES, cfgmgrst_cdbb69b5-e18f-4721-bb66-c6160d959f10.xml, devinst.mem_des'
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MEM_DES, *PMEM_DES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Mem_Des_s
 - cfgmgr32/Mem_Des_s
 - PMEM_DES
 - cfgmgr32/PMEM_DES
 - MEM_DES
 - cfgmgr32/MEM_DES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cfgmgr32.h
api_name:
 - MEM_DES
---

# MEM_DES structure


## -description

The MEM_DES structure is used for specifying either a resource list or a resource requirements list that describes memory usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field MD_Count

#### For a resource list:

Zero.



#### For a resource requirements list:

The number of elements in the [MEM_RANGE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-mem_range) array that is included in the [MEM_RESOURCE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-mem_resource) structure.

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

[MEM_RANGE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-mem_range)



[MEM_RESOURCE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-mem_resource)