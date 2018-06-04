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

# _DEVICE_DATA_SET_LB_PROVISIONING_STATE structure


## -description


Output structure for the <b>DeviceDsmAction_Allocation</b> action of the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff560573">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
    control code.


## -struct-fields




### -field Size

The size of this structure, including the bitmap, in bytes.


### -field Version

The version of this structure.


### -field SlabSizeInBytes

The size of a slab, in bytes.


### -field SlabOffsetDeltaInBytes

If the range specified is not aligned to the <b>OptimalUnmapGranularity</b> as returned 
      in <a href="https://msdn.microsoft.com/library/windows/hardware/hh439649">DEVICE_LB_PROVISIONING_DESCRIPTOR</a> 
      structure then the data represented in the <b>SlabAllocationBitMap</b> is offset from the 
      specified range by this amount.


### -field SlabAllocationBitMapBitCount

The number of relevant bits in the bitmap.


### -field SlabAllocationBitMapLength

The number of<b> DWORD</b>s in the bitmap array.


### -field SlabAllocationBitMap

The allocation bitmap containing one bit for each slab. If a bit is set then the corresponding slab is allocated. Otherwise, if a bit is clear, the corresponding slab is unallocated.


## -remarks



Provisioning state information is returned when the <b>Action</b> member of the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552527">DEVICE_MANAGE_DATA_SET_ATTRIBUTES</a> 
     structure is set to <b>DeviceDsmAction_Allocation</b>. The caller should include only one data 
     set range in the system buffer at <b>DataSetRangesOffset</b>.

On return, the system buffer contains a 
     <a href="https://msdn.microsoft.com/library/windows/hardware/hh439656">DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT</a> 
     structure followed by the 
     <b>DEVICE_DATA_SET_LB_PROVISIONING_STATE</b> 
     structure. The 
     <b>DEVICE_DATA_SET_LB_PROVISIONING_STATE</b> 
     structure begins at an offset from the beginning of the system buffer specified by 
     <b>OutputBlockOffset</b> in 
     <b>DEVICE_MANAGE_DATA_SET_ATTRIBUTES_OUTPUT</b>.

Each bit in the allocation bitmap represents a slab mapping within the data set range requested. The bits 
     correspond directly to the slabs in the data set range. This means that bit 0 in the bitmap marks the first slab 
     in the range. A slab is mapped if the bit value = 1 and unmapped if the bit value = 0.

Space for <b>SlabAllocationBitMap</b> should be allocated based on the number of possible 
     slabs in the requested data set range. The <b>SlabAllocationBitMapLength</b> of the bitmap 
     returned is 
     <code>(number_of_slabs / 32) + ((number_of_slabs MOD 32) &gt; 0 ? 1 : 0)</code>.

Slab size is determined by the <b>OptimalUnmapGranularity</b> member of 
     the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439649">DEVICE_LB_PROVISIONING_DESCRIPTOR</a> 
     structure returned from an 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a> 
     control code. The length of the data set range provided should be a multiple of 
     <b>OptimalUnmapGranularity</b>. When the range length is not a multiple of 
     <b>OptimalUnmapGranularity</b>, it is reduced to be a multiple.

If the starting offset in the data set range is not aligned on a slab boundary, a multiple of 
     <b>OptimalUnmapGranularity</b>, the offset will be adjusted to the next boundary. The 
     difference between the requested offset and the adjusted offset is returned in 
     <b>SlabOffsetDeltaInBytes</b>.

If the slab allocation total returned in <b>SlabAllocationBitMapBitCount</b> is not as 
     expected because of data set range alignment or length adjustments, an additional request may be submitted with a 
     data set range modified according to the values in both <b>SlabAllocationBitMapBitCount</b> 
     and <b>SlabOffsetDeltaInBytes</b>. The new range will properly select the slabs left out of 
     the bitmap returned by the previous request.

If the requested slab size is too large (for example if it is larger than the maximum transfer length of the 
    HBA) then the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff560573">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a> 
    can fail with <b>ERROR_INVALID_PARAMETER</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh439649">DEVICE_LB_PROVISIONING_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/85ebbdca-94a0-4467-8d15-ee3a850e1cd9">Device Management Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560573">IOCTL_STORAGE_MANAGE_DATA_SET_ATTRIBUTES</a>
 

 

