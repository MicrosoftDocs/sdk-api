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

# _DRIVE_LAYOUT_INFORMATION_EX structure


## -description


Contains extended information about a drive's partitions.


## -struct-fields




### -field PartitionStyle

The style of the partitions on the drive enumerated by the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/ff563773">PARTITION_STYLE</a> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PARTITION_STYLE_MBR"></a><a id="partition_style_mbr"></a><dl>
<dt><b>PARTITION_STYLE_MBR</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Master boot record (MBR) format.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_STYLE_GPT"></a><a id="partition_style_gpt"></a><dl>
<dt><b>PARTITION_STYLE_GPT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
GUID Partition Table (GPT) format.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_STYLE_RAW"></a><a id="partition_style_raw"></a><dl>
<dt><b>PARTITION_STYLE_RAW</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Partition not formatted in either of the recognized formats—MBR or GPT.

</td>
</tr>
</table>
 


### -field PartitionCount

The number of partitions on the drive. On hard disks with the MBR layout, this value will always be a 
      multiple of 4. Any partitions that are actually unused will have a partition type of 
      <b>PARTITION_ENTRY_UNUSED</b> (0) set in the <b>PartitionType</b> member 
      of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563767">PARTITION_INFORMATION_MBR</a> structure 
      of the <b>Mbr</b> member of the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/ff563754">PARTITION_INFORMATION_EX</a> structure of the 
      <b>PartitionEntry</b> member of this structure.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.Mbr

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff552668">DRIVE_LAYOUT_INFORMATION_MBR</a> 
       structure containing information about the master boot record type partitioning on the drive.


### -field DUMMYUNIONNAME.Gpt

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff552664">DRIVE_LAYOUT_INFORMATION_GPT</a> 
       structure containing information about the GUID disk partition type partitioning on the drive.


### -field PartitionEntry

A variable-sized array of 
      <a href="https://msdn.microsoft.com/library/windows/hardware/ff563754">PARTITION_INFORMATION_EX</a> structures, one 
      structure for each partition on the drive.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552664">DRIVE_LAYOUT_INFORMATION_GPT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552668">DRIVE_LAYOUT_INFORMATION_MBR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560364">IOCTL_DISK_GET_DRIVE_LAYOUT_EX</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560411">IOCTL_DISK_SET_DRIVE_LAYOUT_EX</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563754">PARTITION_INFORMATION_EX</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563773">PARTITION_STYLE</a>
 

 

