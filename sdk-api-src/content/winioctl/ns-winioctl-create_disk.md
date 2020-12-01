---
UID: NS:winioctl._CREATE_DISK
title: CREATE_DISK
description: Contains information that the IOCTL_DISK_CREATE_DISK control code uses to initialize GUID partition table (GPT), master boot record (MBR), or raw disks.
helpviewer_keywords: ["*PCREATE_DISK","CREATE_DISK","CREATE_DISK structure [Files]","PCREATE_DISK","PCREATE_DISK structure pointer [Files]","_win32_create_disk_str","base.create_disk_str","fs.create_disk_str","winioctl/CREATE_DISK","winioctl/PCREATE_DISK"]
old-location: fs\create_disk_str.htm
tech.root: fs
ms.assetid: ec4a1ef9-ff2e-41b3-951b-241c545f256b
ms.date: 12/05/2018
ms.keywords: '*PCREATE_DISK, CREATE_DISK, CREATE_DISK structure [Files], PCREATE_DISK, PCREATE_DISK structure pointer [Files], _win32_create_disk_str, base.create_disk_str, fs.create_disk_str, winioctl/CREATE_DISK, winioctl/PCREATE_DISK'
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
req.typenames: CREATE_DISK, *PCREATE_DISK
req.redist: 
f1_keywords:
 - _CREATE_DISK
 - winioctl/_CREATE_DISK
 - PCREATE_DISK
 - winioctl/PCREATE_DISK
 - CREATE_DISK
 - winioctl/CREATE_DISK
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
 - CREATE_DISK
---

# CREATE_DISK structure


## -description

Contains information that the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_create_disk">IOCTL_DISK_CREATE_DISK</a> control code uses to initialize GUID partition table (GPT), master boot record (MBR), or raw disks.

## -struct-fields

### -field PartitionStyle

The format of a partition. 

For more information, see 
<a href="/windows/desktop/api/winioctl/ne-winioctl-partition_style">PARTITION_STYLE</a>.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Mbr

A 
<a href="/windows/desktop/api/winioctl/ns-winioctl-create_disk_mbr">CREATE_DISK_MBR</a> structure that contains disk information when an MBR disk is to be initialized.

### -field DUMMYUNIONNAME.Gpt

A 
<a href="/windows/desktop/api/winioctl/ns-winioctl-create_disk_gpt">CREATE_DISK_GPT</a> structure that contains disk information when a GPT disk is to be initialized.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-create_disk_gpt">CREATE_DISK_GPT</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-create_disk_mbr">CREATE_DISK_MBR</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_create_disk">IOCTL_DISK_CREATE_DISK</a>



<a href="/windows/desktop/api/winioctl/ne-winioctl-partition_style">PARTITION_STYLE</a>