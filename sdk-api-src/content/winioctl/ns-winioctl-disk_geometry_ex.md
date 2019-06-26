---
UID: NS:winioctl._DISK_GEOMETRY_EX
title: DISK_GEOMETRY_EX
author: windows-sdk-content
description: Describes the extended geometry of disk devices and media.
old-location: fs\disk_geometry_ex_str.htm
tech.root: FileIO
ms.assetid: 2b8b2021-8650-452d-a975-54249620d72f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDISK_GEOMETRY_EX, DISK_GEOMETRY_EX, DISK_GEOMETRY_EX structure [Files], PDISK_GEOMETRY_EX, PDISK_GEOMETRY_EX structure pointer [Files], _win32_disk_geometry_ex_str, base.disk_geometry_ex_str, fs.disk_geometry_ex_str, winioctl/DISK_GEOMETRY_EX, winioctl/PDISK_GEOMETRY_EX"
ms.topic: struct
f1_keywords: 
 - "winioctl/DISK_GEOMETRY_EX"
req.header: winioctl.h
req.include-header: Windows.h
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
 - WinIoCtl.h
api_name:
 - DISK_GEOMETRY_EX
product: Windows
targetos: Windows
req.typenames: DISK_GEOMETRY_EX, *PDISK_GEOMETRY_EX
req.redist: 
---

# DISK_GEOMETRY_EX structure


## -description


Describes the extended geometry of disk devices and media.


## -struct-fields




### -field Geometry

A <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_disk_geometry">DISK_GEOMETRY</a> structure.


### -field DiskSize

The disk size, in bytes. See <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_large_integer">LARGE_INTEGER</a>.


### -field Data

Any additional data. For more information, see Remarks.


## -remarks



<b>DISK_GEOMETRY_EX</b> is a variable-length structure 
    composed of a <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_disk_geometry">DISK_GEOMETRY</a> structure followed by a 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_disk_partition_info">DISK_PARTITION_INFO</a> structure and a 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_disk_detection_info">DISK_DETECTION_INFO</a> structure. Because the 
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
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_disk_partition_info">DISK_PARTITION_INFO</a> structure.

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
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_partition_information">PARTITION_INFORMATION</a> structure. To obtain 
    this information, use the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_layout_ex">IOCTL_DISK_GET_DRIVE_LAYOUT_EX</a> control code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_disk_detection_info">DISK_DETECTION_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_disk_geometry">DISK_GEOMETRY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_disk_partition_info">DISK_PARTITION_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_geometry_ex">IOCTL_DISK_GET_DRIVE_GEOMETRY_EX</a>
 

 

