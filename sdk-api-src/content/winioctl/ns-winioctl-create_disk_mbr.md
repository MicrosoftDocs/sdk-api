---
UID: NS:winioctl._CREATE_DISK_MBR
title: CREATE_DISK_MBR
description: Contains information that the IOCTL_DISK_CREATE_DISK control code uses to initialize master boot record (MBR) disks.
helpviewer_keywords: ["*PCREATE_DISK_MBR","CREATE_DISK_MBR","CREATE_DISK_MBR structure [Files]","PCREATE_DISK_MBR","PCREATE_DISK_MBR structure pointer [Files]","_win32_create_disk_mbr_str","base.create_disk_mbr_str","fs.create_disk_mbr_str","winioctl/CREATE_DISK_MBR","winioctl/PCREATE_DISK_MBR"]
old-location: fs\create_disk_mbr_str.htm
tech.root: fs
ms.assetid: 6b475622-371d-4097-9de1-6ef31af76322
ms.date: 12/05/2018
ms.keywords: '*PCREATE_DISK_MBR, CREATE_DISK_MBR, CREATE_DISK_MBR structure [Files], PCREATE_DISK_MBR, PCREATE_DISK_MBR structure pointer [Files], _win32_create_disk_mbr_str, base.create_disk_mbr_str, fs.create_disk_mbr_str, winioctl/CREATE_DISK_MBR, winioctl/PCREATE_DISK_MBR'
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
req.typenames: CREATE_DISK_MBR, *PCREATE_DISK_MBR
req.redist: 
f1_keywords:
 - _CREATE_DISK_MBR
 - winioctl/_CREATE_DISK_MBR
 - PCREATE_DISK_MBR
 - winioctl/PCREATE_DISK_MBR
 - CREATE_DISK_MBR
 - winioctl/CREATE_DISK_MBR
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
 - CREATE_DISK_MBR
---

# CREATE_DISK_MBR structure


## -description

Contains information that the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_create_disk">IOCTL_DISK_CREATE_DISK</a> control code uses to initialize master boot record (MBR) disks.

## -struct-fields

### -field Signature

The disk signature of the MBR disk to be initialized.

## -remarks

The 
<b>CREATE_DISK_MBR</b> structure is part of the 
<a href="/windows/desktop/api/winioctl/ns-winioctl-create_disk">CREATE_DISK</a> structure.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-create_disk">CREATE_DISK</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-create_disk_gpt">CREATE_DISK_GPT</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_create_disk">IOCTL_DISK_CREATE_DISK</a>