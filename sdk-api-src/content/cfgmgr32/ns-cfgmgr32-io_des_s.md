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

# IO_Des_s structure


## -description


The IO_DES structure is used for specifying either a resource list or a resource requirements list that describes I/O port usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff547012">Hardware Resources</a>.


## -struct-fields




### -field IOD_Count





#### For a resource list:

Zero.



#### For a resource requirements list:

The number of elements in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548192">IO_RANGE</a> array that is included in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548201">IO_RESOURCE</a> structure.


### -field IOD_Type

Must be set to the constant value <b>IOType_Range</b>.


### -field IOD_Alloc_Base





#### For a resource list:

The lowest-numbered of a range of contiguous I/O port addresses allocated to the device.



#### For a resource requirements list:

Zero.


### -field IOD_Alloc_End





#### For a resource list:

The highest-numbered of a range of contiguous I/O port addresses allocated to the device.



#### For a resource requirements list:

Zero.


### -field IOD_DesFlags

One bit flag from <i>each</i> of the flag sets described in the following table.

<table>
<tr>
<th></th>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td colspan="2">
<i>Port Type Flags</i>

</td>
<td></td>
</tr>
<tr>
<td></td>
<td>
<b>fIOD_IO</b>

</td>
<td>
The device is accessed in I/O address space.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fIOD_Memory</b>

</td>
<td>
The device is accessed in memory address space.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fIOD_PortType</b>

</td>
<td>
Bitmask for the bits within <b>IOD_DesFlags</b> that specify the port type value.

</td>
</tr>
<tr>
<td colspan="2">
<i>Decode Flags</i>

</td>
<td></td>
</tr>
<tr>
<td></td>
<td>
<b>fIOD_10_BIT_DECODE</b>

</td>
<td>
The device decodes 10 bits of the port address.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fIOD_12_BIT_DECODE</b>

</td>
<td>
The device decodes 12 bits of the port address.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fIOD_16_BIT_DECODE</b>

</td>
<td>
The device decodes 16 bits of the port address.

</td>
</tr>
<tr>
<td></td>
<td>
<b>fIOD_POSITIVE_DECODE</b>

</td>
<td>
The device uses "positive decode" instead of "subtractive decode."

</td>
</tr>
<tr>
<td></td>
<td>
<b>fIOD_DECODE</b>

</td>
<td>
Bitmask for the bits within <b>IOD_DesFlags</b> that specify the decode value.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548192">IO_RANGE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548201">IO_RESOURCE</a>
 

 

