---
UID: NS:winioctl._DISK_GEOMETRY
title: DISK_GEOMETRY
description: Describes the geometry of disk devices and media.
helpviewer_keywords: ["*PDISK_GEOMETRY","DISK_GEOMETRY","DISK_GEOMETRY structure [Files]","_win32_disk_geometry_str","base.disk_geometry_str","fs.disk_geometry_str","winioctl/DISK_GEOMETRY"]
old-location: fs\disk_geometry_str.htm
tech.root: fs
ms.assetid: 5e5955b4-1319-42c9-9df8-9910c05dec69
ms.date: 12/05/2018
ms.keywords: '*PDISK_GEOMETRY, DISK_GEOMETRY, DISK_GEOMETRY structure [Files], _win32_disk_geometry_str, base.disk_geometry_str, fs.disk_geometry_str, winioctl/DISK_GEOMETRY'
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
req.typenames: DISK_GEOMETRY, *PDISK_GEOMETRY
req.redist: 
f1_keywords:
 - _DISK_GEOMETRY
 - winioctl/_DISK_GEOMETRY
 - PDISK_GEOMETRY
 - winioctl/PDISK_GEOMETRY
 - DISK_GEOMETRY
 - winioctl/DISK_GEOMETRY
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
 - DISK_GEOMETRY
---

# DISK_GEOMETRY structure


## -description

Describes the geometry of disk devices and media.

## -struct-fields

### -field Cylinders

The number of cylinders. See [**LARGE_INTEGER**](../winnt/ns-winnt-large_integer-r1.md).

### -field MediaType

The type of media. For a list of values, see [MEDIA_TYPE](ne-winioctl-media_type.md).

### -field TracksPerCylinder

The number of tracks per cylinder.

### -field SectorsPerTrack

The number of sectors per track.

### -field BytesPerSector

The number of bytes per sector.

## -see-also

[IOCTL_DISK_GET_DRIVE_GEOMETRY](ni-winioctl-ioctl_disk_get_drive_geometry.md), [IOCTL_STORAGE_GET_MEDIA_TYPES](ni-winioctl-ioctl_storage_get_media_types.md), [MEDIA_TYPE](ne-winioctl-media_type.md)

