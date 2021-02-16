---
UID: NE:winioctl._PARTITION_STYLE
title: PARTITION_STYLE
description: Represents the format of a partition.
helpviewer_keywords: ["PARTITION_STYLE","PARTITION_STYLE enumeration [Files]","PARTITION_STYLE_GPT","PARTITION_STYLE_MBR","PARTITION_STYLE_RAW","_win32_partition_style_str","base.partition_style_str","fs.partition_style_str","winioctl/PARTITION_STYLE","winioctl/PARTITION_STYLE_GPT","winioctl/PARTITION_STYLE_MBR","winioctl/PARTITION_STYLE_RAW"]
old-location: fs\partition_style_str.htm
tech.root: fs
ms.assetid: 254e4ea1-d0c8-4033-b8af-e5dbfb7c7da8
ms.date: 12/05/2018
ms.keywords: PARTITION_STYLE, PARTITION_STYLE enumeration [Files], PARTITION_STYLE_GPT, PARTITION_STYLE_MBR, PARTITION_STYLE_RAW, _win32_partition_style_str, base.partition_style_str, fs.partition_style_str, winioctl/PARTITION_STYLE, winioctl/PARTITION_STYLE_GPT, winioctl/PARTITION_STYLE_MBR, winioctl/PARTITION_STYLE_RAW
req.header: winioctl.h
req.include-header: 
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
req.typenames: PARTITION_STYLE
req.redist: 
f1_keywords:
 - _PARTITION_STYLE
 - winioctl/_PARTITION_STYLE
 - PARTITION_STYLE
 - winioctl/PARTITION_STYLE
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
 - PARTITION_STYLE
---

# PARTITION_STYLE enumeration


## -description

Represents the format of a partition.

## -enum-fields

### -field PARTITION_STYLE_MBR

Master boot record (MBR) format. This corresponds to standard *AT-style* MBR partitions.

### -field PARTITION_STYLE_GPT

GUID Partition Table (GPT) format.

### -field PARTITION_STYLE_RAW

Partition not formatted in either of the recognized formats—MBR or GPT.

## -see-also

* [File System Recognition](/windows/desktop/FileIO/file-system-recognition)
* [IOCTL_DISK_GET_PARTITION_INFO_EX](ni-winioctl-ioctl_disk_get_partition_info_ex.md)
* [IOCTL_DISK_SET_PARTITION_INFO_EX](ni-winioctl-ioctl_disk_set_partition_info_ex.md)
* [PARTITION_INFORMATION_EX](ns-winioctl-partition_information_ex.md)