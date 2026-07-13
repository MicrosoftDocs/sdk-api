---
UID: NS:winioctl._DRIVE_LAYOUT_INFORMATION_GPT
title: DRIVE_LAYOUT_INFORMATION_GPT
description: Contains information about a drive's GUID partition table (GPT) partitions.
helpviewer_keywords: ["*PDRIVE_LAYOUT_INFORMATION_GPT","DRIVE_LAYOUT_INFORMATION_GPT","DRIVE_LAYOUT_INFORMATION_GPT structure [Files]","PDRIVE_LAYOUT_INFORMATION_GPT","PDRIVE_LAYOUT_INFORMATION_GPT structure pointer [Files]","_win32_drive_layout_information_gpt_str","base.drive_layout_information_gpt_str","fs.drive_layout_information_gpt_str","winioctl/DRIVE_LAYOUT_INFORMATION_GPT","winioctl/PDRIVE_LAYOUT_INFORMATION_GPT"]
old-location: fs\drive_layout_information_gpt_str.htm
tech.root: fs
ms.assetid: 763b0d64-6dcc-411c-aca1-3beea0890124
ms.date: 12/05/2018
ms.keywords: '*PDRIVE_LAYOUT_INFORMATION_GPT, DRIVE_LAYOUT_INFORMATION_GPT, DRIVE_LAYOUT_INFORMATION_GPT structure [Files], PDRIVE_LAYOUT_INFORMATION_GPT, PDRIVE_LAYOUT_INFORMATION_GPT structure pointer [Files], _win32_drive_layout_information_gpt_str, base.drive_layout_information_gpt_str, fs.drive_layout_information_gpt_str, winioctl/DRIVE_LAYOUT_INFORMATION_GPT, winioctl/PDRIVE_LAYOUT_INFORMATION_GPT'
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
targetos: Windows
req.typenames: DRIVE_LAYOUT_INFORMATION_GPT, *PDRIVE_LAYOUT_INFORMATION_GPT
req.redist: 
f1_keywords:
 - _DRIVE_LAYOUT_INFORMATION_GPT
 - winioctl/_DRIVE_LAYOUT_INFORMATION_GPT
 - PDRIVE_LAYOUT_INFORMATION_GPT
 - winioctl/PDRIVE_LAYOUT_INFORMATION_GPT
 - DRIVE_LAYOUT_INFORMATION_GPT
 - winioctl/DRIVE_LAYOUT_INFORMATION_GPT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - DRIVE_LAYOUT_INFORMATION_GPT
---

# DRIVE_LAYOUT_INFORMATION_GPT structure


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

<a href="/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information_ex">DRIVE_LAYOUT_INFORMATION_EX</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information_mbr">DRIVE_LAYOUT_INFORMATION_MBR</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_layout_ex">IOCTL_DISK_GET_DRIVE_LAYOUT_EX</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout_ex">IOCTL_DISK_SET_DRIVE_LAYOUT_EX</a>