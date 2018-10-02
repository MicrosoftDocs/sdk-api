---
UID: NS:winioctl._DRIVE_LAYOUT_INFORMATION
title: "_DRIVE_LAYOUT_INFORMATION"
author: windows-sdk-content
description: Contains information about the partitions of a drive.
old-location: fs\drive_layout_information_str.htm
tech.root: fileio
ms.assetid: e67ccaa7-a735-4695-8385-28f57b41821c
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: "*PDRIVE_LAYOUT_INFORMATION, DRIVE_LAYOUT_INFORMATION, DRIVE_LAYOUT_INFORMATION structure [Files], PDRIVE_LAYOUT_INFORMATION, PDRIVE_LAYOUT_INFORMATION structure pointer [Files], _DRIVE_LAYOUT_INFORMATION, _win32_drive_layout_information_str, base.drive_layout_information_str, fs.drive_layout_information_str, winioctl/DRIVE_LAYOUT_INFORMATION, winioctl/PDRIVE_LAYOUT_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
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
 - DRIVE_LAYOUT_INFORMATION
product: Windows
targetos: Windows
req.typenames: DRIVE_LAYOUT_INFORMATION, *PDRIVE_LAYOUT_INFORMATION
req.redist: 
---

# _DRIVE_LAYOUT_INFORMATION structure


## -description


Contains information about the partitions of a drive.
<div class="alert"><b>Note</b>  <b>DRIVE_LAYOUT_INFORMATION</b> is superseded 
    by the <a href="https://msdn.microsoft.com/381c87a8-fe40-4251-a4df-dddc9e2a126d">DRIVE_LAYOUT_INFORMATION_EX</a> 
    structure.</div><div> </div>

## -struct-fields




### -field PartitionCount

The number of partitions on a drive.

On disks with the MBR layout, this value is always a multiple of 4. Any partitions that are unused have a 
       partition type of <b>PARTITION_ENTRY_UNUSED</b> (0).


### -field Signature

The drive signature value. 
     


### -field PartitionEntry

A variable-sized array of 
      <a href="https://msdn.microsoft.com/2c8fa83a-0694-4e17-a9e4-87f839a0d458">PARTITION_INFORMATION</a> structures, one 
      structure for each partition on a drive.


## -see-also




<a href="https://msdn.microsoft.com/381c87a8-fe40-4251-a4df-dddc9e2a126d">DRIVE_LAYOUT_INFORMATION_EX</a>



<a href="https://msdn.microsoft.com/6c1bc445-3cd1-4f86-a36b-f74ad8f4d2e5">IOCTL_DISK_GET_DRIVE_LAYOUT</a>



<a href="https://msdn.microsoft.com/8cace6a5-666a-4d35-a557-6bf0564dbe58">IOCTL_DISK_SET_DRIVE_LAYOUT</a>
 

 

