---
UID: NS:winioctl._DRIVE_LAYOUT_INFORMATION_EX
title: DRIVE_LAYOUT_INFORMATION_EX (winioctl.h)
author: windows-sdk-content
description: Contains extended information about a drive's partitions.
old-location: fs\drive_layout_information_ex_str.htm
tech.root: FileIO
ms.assetid: 381c87a8-fe40-4251-a4df-dddc9e2a126d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDRIVE_LAYOUT_INFORMATION_EX, DRIVE_LAYOUT_INFORMATION_EX, DRIVE_LAYOUT_INFORMATION_EX structure [Files], PARTITION_STYLE_GPT, PARTITION_STYLE_MBR, PARTITION_STYLE_RAW, PDRIVE_LAYOUT_INFORMATION_EX, PDRIVE_LAYOUT_INFORMATION_EX structure pointer [Files], _win32_drive_layout_information_ex_str, base.drive_layout_information_ex_str, fs.drive_layout_information_ex_str, winioctl/DRIVE_LAYOUT_INFORMATION_EX, winioctl/PDRIVE_LAYOUT_INFORMATION_EX"
ms.topic: struct
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
 - DRIVE_LAYOUT_INFORMATION_EX
product: Windows
targetos: Windows
req.typenames: DRIVE_LAYOUT_INFORMATION_EX, *PDRIVE_LAYOUT_INFORMATION_EX
req.redist: 
---

# DRIVE_LAYOUT_INFORMATION_EX structure


## -description


Contains extended information about a drive's partitions.


## -struct-fields




### -field PartitionStyle

The style of the partitions on the drive enumerated by the 
      <a href="https://msdn.microsoft.com/254e4ea1-d0c8-4033-b8af-e5dbfb7c7da8">PARTITION_STYLE</a> enumeration.

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
      of the <a href="https://msdn.microsoft.com/5b74b06f-ef4c-44ab-95c6-49c050faf1f4">PARTITION_INFORMATION_MBR</a> structure 
      of the <b>Mbr</b> member of the 
      <a href="https://msdn.microsoft.com/3c88ebae-274e-403a-8f57-58fdf863f511">PARTITION_INFORMATION_EX</a> structure of the 
      <b>PartitionEntry</b> member of this structure.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.Mbr

A <a href="https://msdn.microsoft.com/71c361fe-8c85-4915-9776-8ad3f5837e11">DRIVE_LAYOUT_INFORMATION_MBR</a> 
       structure containing information about the master boot record type partitioning on the drive.


### -field DUMMYUNIONNAME.Gpt

A <a href="https://msdn.microsoft.com/763b0d64-6dcc-411c-aca1-3beea0890124">DRIVE_LAYOUT_INFORMATION_GPT</a> 
       structure containing information about the GUID disk partition type partitioning on the drive.


### -field PartitionEntry

A variable-sized array of 
      <a href="https://msdn.microsoft.com/3c88ebae-274e-403a-8f57-58fdf863f511">PARTITION_INFORMATION_EX</a> structures, one 
      structure for each partition on the drive.


## -see-also




<a href="https://msdn.microsoft.com/763b0d64-6dcc-411c-aca1-3beea0890124">DRIVE_LAYOUT_INFORMATION_GPT</a>



<a href="https://msdn.microsoft.com/71c361fe-8c85-4915-9776-8ad3f5837e11">DRIVE_LAYOUT_INFORMATION_MBR</a>



<a href="https://msdn.microsoft.com/21507182-5a33-4e58-b5ed-3724feefa4ed">IOCTL_DISK_GET_DRIVE_LAYOUT_EX</a>



<a href="https://msdn.microsoft.com/8cace6a5-666a-4d35-a557-6bf0564dbe58">IOCTL_DISK_SET_DRIVE_LAYOUT_EX</a>



<a href="https://msdn.microsoft.com/3c88ebae-274e-403a-8f57-58fdf863f511">PARTITION_INFORMATION_EX</a>



<a href="https://msdn.microsoft.com/254e4ea1-d0c8-4033-b8af-e5dbfb7c7da8">PARTITION_STYLE</a>
 

 

