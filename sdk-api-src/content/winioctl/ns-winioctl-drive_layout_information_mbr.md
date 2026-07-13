---
UID: NS:winioctl._DRIVE_LAYOUT_INFORMATION_MBR
title: DRIVE_LAYOUT_INFORMATION_MBR
description: Provides information about a drive's master boot record (MBR) partitions.
helpviewer_keywords: ["*PDRIVE_LAYOUT_INFORMATION_MBR","DRIVE_LAYOUT_INFORMATION_MBR","DRIVE_LAYOUT_INFORMATION_MBR structure [Files]","PDRIVE_LAYOUT_INFORMATION_MBR","PDRIVE_LAYOUT_INFORMATION_MBR structure pointer [Files]","_win32_drive_layout_information_mbr_str","base.drive_layout_information_mbr_str","fs.drive_layout_information_mbr_str","winioctl/DRIVE_LAYOUT_INFORMATION_MBR","winioctl/PDRIVE_LAYOUT_INFORMATION_MBR"]
old-location: fs\drive_layout_information_mbr_str.htm
tech.root: fs
ms.assetid: 71c361fe-8c85-4915-9776-8ad3f5837e11
ms.date: 12/05/2018
ms.keywords: '*PDRIVE_LAYOUT_INFORMATION_MBR, DRIVE_LAYOUT_INFORMATION_MBR, DRIVE_LAYOUT_INFORMATION_MBR structure [Files], PDRIVE_LAYOUT_INFORMATION_MBR, PDRIVE_LAYOUT_INFORMATION_MBR structure pointer [Files], _win32_drive_layout_information_mbr_str, base.drive_layout_information_mbr_str, fs.drive_layout_information_mbr_str, winioctl/DRIVE_LAYOUT_INFORMATION_MBR, winioctl/PDRIVE_LAYOUT_INFORMATION_MBR'
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
req.typenames: DRIVE_LAYOUT_INFORMATION_MBR, *PDRIVE_LAYOUT_INFORMATION_MBR
req.redist: 
f1_keywords:
 - _DRIVE_LAYOUT_INFORMATION_MBR
 - winioctl/_DRIVE_LAYOUT_INFORMATION_MBR
 - PDRIVE_LAYOUT_INFORMATION_MBR
 - winioctl/PDRIVE_LAYOUT_INFORMATION_MBR
 - DRIVE_LAYOUT_INFORMATION_MBR
 - winioctl/DRIVE_LAYOUT_INFORMATION_MBR
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
 - DRIVE_LAYOUT_INFORMATION_MBR
---

# DRIVE_LAYOUT_INFORMATION_MBR structure


## -description

Provides information about a drive's master boot record (MBR) partitions.

## -struct-fields

### -field Signature

The signature of the drive.

### -field CheckSum

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information_ex">DRIVE_LAYOUT_INFORMATION_EX</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information_gpt">DRIVE_LAYOUT_INFORMATION_GPT</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_layout_ex">IOCTL_DISK_GET_DRIVE_LAYOUT_EX</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout_ex">IOCTL_DISK_SET_DRIVE_LAYOUT_EX</a>