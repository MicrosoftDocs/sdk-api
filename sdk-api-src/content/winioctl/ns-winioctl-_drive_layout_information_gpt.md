---
UID: NS:winioctl._DRIVE_LAYOUT_INFORMATION_GPT
title: "_DRIVE_LAYOUT_INFORMATION_GPT"
author: windows-sdk-content
description: Contains information about a drive's GUID partition table (GPT) partitions.
old-location: fs\drive_layout_information_gpt_str.htm
old-project: FileIO
ms.assetid: 763b0d64-6dcc-411c-aca1-3beea0890124
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PDRIVE_LAYOUT_INFORMATION_GPT, DRIVE_LAYOUT_INFORMATION_GPT, DRIVE_LAYOUT_INFORMATION_GPT structure [Files], PDRIVE_LAYOUT_INFORMATION_GPT, PDRIVE_LAYOUT_INFORMATION_GPT structure pointer [Files], _DRIVE_LAYOUT_INFORMATION_GPT, _win32_drive_layout_information_gpt_str, base.drive_layout_information_gpt_str, fs.drive_layout_information_gpt_str, winioctl/DRIVE_LAYOUT_INFORMATION_GPT, winioctl/PDRIVE_LAYOUT_INFORMATION_GPT"
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
tech.root: 
req.typenames: DRIVE_LAYOUT_INFORMATION_GPT, *PDRIVE_LAYOUT_INFORMATION_GPT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - DRIVE_LAYOUT_INFORMATION_GPT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _DRIVE_LAYOUT_INFORMATION_GPT structure


## -description


Contains information about a drive's GUID partition table (GPT) partitions.


## -struct-fields




### -field DiskId

The <b>GUID</b> of the disk.


### -field StartingUsableOffset

The starting byte offset of the first usable block.


### -field UsableLength

The size of the usable blocks on the disk, in bytes.


### -field MaxPartitionCount

The maximum number of partitions that can be defined in the usable block.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552662">DRIVE_LAYOUT_INFORMATION_EX</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552668">DRIVE_LAYOUT_INFORMATION_MBR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560364">IOCTL_DISK_GET_DRIVE_LAYOUT_EX</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560411">IOCTL_DISK_SET_DRIVE_LAYOUT_EX</a>
 

 

