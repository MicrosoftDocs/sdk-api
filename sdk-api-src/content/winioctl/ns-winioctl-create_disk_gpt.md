---
UID: NS:winioctl._CREATE_DISK_GPT
title: CREATE_DISK_GPT
description: Contains information used by the IOCTL_DISK_CREATE_DISK control code to initialize GUID partition table (GPT) disks.
helpviewer_keywords: ["*PCREATE_DISK_GPT","CREATE_DISK_GPT","CREATE_DISK_GPT structure [Files]","PCREATE_DISK_GPT","PCREATE_DISK_GPT structure pointer [Files]","_win32_create_disk_gpt_str","base.create_disk_gpt_str","fs.create_disk_gpt_str","winioctl/CREATE_DISK_GPT","winioctl/PCREATE_DISK_GPT"]
old-location: fs\create_disk_gpt_str.htm
tech.root: fs
ms.assetid: 526a265b-e15e-4cd2-adaf-c955a8cb92e5
ms.date: 12/05/2018
ms.keywords: '*PCREATE_DISK_GPT, CREATE_DISK_GPT, CREATE_DISK_GPT structure [Files], PCREATE_DISK_GPT, PCREATE_DISK_GPT structure pointer [Files], _win32_create_disk_gpt_str, base.create_disk_gpt_str, fs.create_disk_gpt_str, winioctl/CREATE_DISK_GPT, winioctl/PCREATE_DISK_GPT'
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
req.typenames: CREATE_DISK_GPT, *PCREATE_DISK_GPT
req.redist: 
f1_keywords:
 - _CREATE_DISK_GPT
 - winioctl/_CREATE_DISK_GPT
 - PCREATE_DISK_GPT
 - winioctl/PCREATE_DISK_GPT
 - CREATE_DISK_GPT
 - winioctl/CREATE_DISK_GPT
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
 - CREATE_DISK_GPT
---

# CREATE_DISK_GPT structure


## -description

Contains information used by the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_create_disk">IOCTL_DISK_CREATE_DISK</a> control code to initialize GUID partition table (GPT) disks.

## -struct-fields

### -field DiskId

The disk identifier (GUID) of the GPT disk to be initialized.

### -field MaxPartitionCount

The maximum number of partitions allowed on the GPT disk to be initialized without repartitioning the disk.

## -remarks

The 
<b>CREATE_DISK_GPT</b> structure is defined as part of the 
<a href="/windows/desktop/api/winioctl/ns-winioctl-create_disk">CREATE_DISK</a> structure.

If a maximum partition count of less than 128 is specified, it will be reset to 128. This is in compliance with the EFI specification.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-create_disk">CREATE_DISK</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-create_disk_mbr">CREATE_DISK_MBR</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_create_disk">IOCTL_DISK_CREATE_DISK</a>