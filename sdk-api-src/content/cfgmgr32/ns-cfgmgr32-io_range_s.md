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

# IO_Range_s structure


## -description


The IO_RANGE structure specifies a resource requirements list that describes I/O port usage for a device instance. For more information about resource requirements lists, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff547012">Hardware Resources</a>.


## -struct-fields




### -field IOR_Align

Mask used to specify the port address boundary on which the first allocated I/O port address must be aligned.


### -field IOR_nPorts

The number of I/O port addresses required by the device.


### -field IOR_Min

The lowest-numbered of a range of contiguous I/O port addresses that can be allocated to the device.


### -field IOR_Max

The highest-numbered of a range of contiguous I/O port addresses that can be allocated to the device.


### -field IOR_RangeFlags

One bit flag from <i>each</i> of the flag sets described in the table included with the description of the <b>IOD_DesFlags</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548184">IO_DES</a> structure. For more information, see the following <b>Remarks</b> section.


### -field IOR_Alias

One of the bit flags described in the following table.

<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
IO_ALIAS_10_BIT_DECODE

</td>
<td>
The device decodes 10 bits of the port address.

</td>
</tr>
<tr>
<td>
IO_ALIAS_12_BIT_DECODE

</td>
<td>
The device decodes 12 bits of the port address.

</td>
</tr>
<tr>
<td>
IO_ALIAS_16_BIT_DECODE

</td>
<td>
The device decodes 16 bits of the port address.

</td>
</tr>
<tr>
<td>
IO_ALIAS_POSITIVE_DECODE

</td>
<td>
The device uses "positive decode" instead of "subtractive decode."

</td>
</tr>
</table>
 

For more information, see the following <b>Remarks</b> section.


## -remarks



The flags specified for <b>IOR_Alias</b> have the same interpretation as the address decoding flags specified for <b>IOD_DesFlags</b>. (However, the two sets of flags are not equivalent in assigned values and cannot be used interchangeably.) A resource requirements list can be specified using either set of flags, but using decode flags in <b>IOD_DesFlags</b> is recommended. If address decoding flags are specified using <i>both</i><b>IOD_DesFlags</b> and <b>IOR_Alias</b>, contents of the latter overrides the former.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548184">IO_DES</a>
 

 

