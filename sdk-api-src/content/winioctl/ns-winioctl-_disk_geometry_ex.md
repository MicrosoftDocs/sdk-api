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

# _DISK_GEOMETRY_EX structure


## -description


Describes the extended geometry of disk devices and media.


## -struct-fields




### -field Geometry

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff552613">DISK_GEOMETRY</a> structure.


### -field DiskSize

The disk size, in bytes. See <a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>.


### -field Data

Any additional data. For more information, see Remarks.


## -remarks



<b>DISK_GEOMETRY_EX</b> is a variable-length structure 
    composed of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff552613">DISK_GEOMETRY</a> structure followed by a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff552629">DISK_PARTITION_INFO</a> structure and a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff552601">DISK_DETECTION_INFO</a> structure. Because the 
    detection information is not at a fixed location within the 
    <b>DISK_GEOMETRY_EX</b> structure, use the following 
    macro to access the <b>DISK_DETECTION_INFO</b> structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
PDISK_DETECTION_INFO DiskGeometryGetDetect(
  PDISK_GEOMETRY_EX Geometry
);</pre>
</td>
</tr>
</table></span></div>

    Similarly, use the following macro to access the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff552629">DISK_PARTITION_INFO</a> structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
PDISK_PARTITION_INFO DiskGeometryGetPartition(
  PDISK_GEOMETRY_EX Geometry
);</pre>
</td>
</tr>
</table></span></div>

    The information returned does not include the number of partitions nor the partition information contained in the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff563751">PARTITION_INFORMATION</a> structure. To obtain 
    this information, use the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff560364">IOCTL_DISK_GET_DRIVE_LAYOUT_EX</a> control code.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552601">DISK_DETECTION_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552613">DISK_GEOMETRY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552629">DISK_PARTITION_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560359">IOCTL_DISK_GET_DRIVE_GEOMETRY_EX</a>
 

 

