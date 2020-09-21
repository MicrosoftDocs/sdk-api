---
UID: NS:winioctl._VOLUME_DISK_EXTENTS
title: VOLUME_DISK_EXTENTS
description: Represents a physical location on a disk.
helpviewer_keywords: ["*PVOLUME_DISK_EXTENTS","PVOLUME_DISK_EXTENTS","PVOLUME_DISK_EXTENTS structure pointer [Files]","VOLUME_DISK_EXTENTS","VOLUME_DISK_EXTENTS structure [Files]","_win32_volume_disk_extents_str","base.volume_disk_extents_str","fs.volume_disk_extents_str","winioctl/PVOLUME_DISK_EXTENTS","winioctl/VOLUME_DISK_EXTENTS"]
old-location: fs\volume_disk_extents_str.htm
tech.root: fs
ms.assetid: 3f38f03c-1b99-4072-904c-dca1b98a245c
ms.date: 12/05/2018
ms.keywords: '*PVOLUME_DISK_EXTENTS, PVOLUME_DISK_EXTENTS, PVOLUME_DISK_EXTENTS structure pointer [Files], VOLUME_DISK_EXTENTS, VOLUME_DISK_EXTENTS structure [Files], _win32_volume_disk_extents_str, base.volume_disk_extents_str, fs.volume_disk_extents_str, winioctl/PVOLUME_DISK_EXTENTS, winioctl/VOLUME_DISK_EXTENTS'
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
req.typenames: VOLUME_DISK_EXTENTS, *PVOLUME_DISK_EXTENTS
req.redist: 
f1_keywords:
 - _VOLUME_DISK_EXTENTS
 - winioctl/_VOLUME_DISK_EXTENTS
 - PVOLUME_DISK_EXTENTS
 - winioctl/PVOLUME_DISK_EXTENTS
 - VOLUME_DISK_EXTENTS
 - winioctl/VOLUME_DISK_EXTENTS
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
 - VOLUME_DISK_EXTENTS
---

# VOLUME_DISK_EXTENTS structure


## -description

Represents a physical location on a disk. It is the output buffer for the 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_volume_get_volume_disk_extents">IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS</a> 
    control code.

## -struct-fields

### -field NumberOfDiskExtents

The number of disks in the volume (a volume can span multiple disks).

An extent is a contiguous run of sectors on one disk. When the number of extents returned is greater than 
       one (1), the error code  <b>ERROR_MORE_DATA</b> is returned. You should call 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> again, allocating enough buffer 
       space based on the value of <b>NumberOfDiskExtents</b> after the first 
       <b>DeviceIoControl</b> call.

### -field Extents

An array of <a href="/windows/desktop/api/winioctl/ns-winioctl-disk_extent">DISK_EXTENT</a> structures.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-disk_extent">DISK_EXTENT</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_volume_get_volume_disk_extents">IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS</a>