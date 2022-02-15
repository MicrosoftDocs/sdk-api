---
UID: NE:winioctl._MEDIA_TYPE
title: MEDIA_TYPE
description: Represents the various forms of device media.
helpviewer_keywords: ["*PMEDIA_TYPE","F3_120M_512","F3_128Mb_512","F3_1Pt23_1024","F3_1Pt2_512","F3_1Pt44_512","F3_200Mb_512","F3_20Pt8_512","F3_230Mb_512","F3_240M_512","F3_2Pt88_512","F3_32M_512","F3_640_512","F3_720_512","F5_160_512","F5_180_512","F5_1Pt23_1024","F5_1Pt2_512","F5_320_1024","F5_320_512","F5_360_512","F5_640_512","F5_720_512","F8_256_128","FixedMedia","MEDIA_TYPE","MEDIA_TYPE enumeration [Files]","RemovableMedia","Unknown","_win32_media_type_str","base.media_type_str","fs.media_type_str","winioctl/F3_120M_512","winioctl/F3_128Mb_512","winioctl/F3_1Pt23_1024","winioctl/F3_1Pt2_512","winioctl/F3_1Pt44_512","winioctl/F3_200Mb_512","winioctl/F3_20Pt8_512","winioctl/F3_230Mb_512","winioctl/F3_240M_512","winioctl/F3_2Pt88_512","winioctl/F3_32M_512","winioctl/F3_640_512","winioctl/F3_720_512","winioctl/F5_160_512","winioctl/F5_180_512","winioctl/F5_1Pt23_1024","winioctl/F5_1Pt2_512","winioctl/F5_320_1024","winioctl/F5_320_512","winioctl/F5_360_512","winioctl/F5_640_512","winioctl/F5_720_512","winioctl/F8_256_128","winioctl/FixedMedia","winioctl/MEDIA_TYPE","winioctl/RemovableMedia","winioctl/Unknown"]
old-location: fs\media_type_str.htm
tech.root: fs
ms.assetid: 183cf8fc-c17b-4def-b590-0aa4b67488f6
ms.date: 12/05/2018
ms.keywords: '*PMEDIA_TYPE, F3_120M_512, F3_128Mb_512, F3_1Pt23_1024, F3_1Pt2_512, F3_1Pt44_512, F3_200Mb_512, F3_20Pt8_512, F3_230Mb_512, F3_240M_512, F3_2Pt88_512, F3_32M_512, F3_640_512, F3_720_512, F5_160_512, F5_180_512, F5_1Pt23_1024, F5_1Pt2_512, F5_320_1024, F5_320_512, F5_360_512, F5_640_512, F5_720_512, F8_256_128, FixedMedia, MEDIA_TYPE, MEDIA_TYPE enumeration [Files], RemovableMedia, Unknown, _win32_media_type_str, base.media_type_str, fs.media_type_str, winioctl/F3_120M_512, winioctl/F3_128Mb_512, winioctl/F3_1Pt23_1024, winioctl/F3_1Pt2_512, winioctl/F3_1Pt44_512, winioctl/F3_200Mb_512, winioctl/F3_20Pt8_512, winioctl/F3_230Mb_512, winioctl/F3_240M_512, winioctl/F3_2Pt88_512, winioctl/F3_32M_512, winioctl/F3_640_512, winioctl/F3_720_512, winioctl/F5_160_512, winioctl/F5_180_512, winioctl/F5_1Pt23_1024, winioctl/F5_1Pt2_512, winioctl/F5_320_1024, winioctl/F5_320_512, winioctl/F5_360_512, winioctl/F5_640_512, winioctl/F5_720_512, winioctl/F8_256_128, winioctl/FixedMedia, winioctl/MEDIA_TYPE, winioctl/RemovableMedia, winioctl/Unknown'
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
req.typenames: MEDIA_TYPE, *PMEDIA_TYPE
req.redist: 
f1_keywords:
 - _MEDIA_TYPE
 - winioctl/_MEDIA_TYPE
 - PMEDIA_TYPE
 - winioctl/PMEDIA_TYPE
 - MEDIA_TYPE
 - winioctl/MEDIA_TYPE
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
 - MEDIA_TYPE
---

# MEDIA_TYPE enumeration


## -description

Represents the various forms of device media.

## -enum-fields

### -field Unknown:0

Format is unknown

### -field F5_1Pt2_512

A 5.25" floppy, with 1.2MB and 512 bytes/sector.

### -field F3_1Pt44_512

A 3.5" floppy, with 1.44MB and 512 bytes/sector.

### -field F3_2Pt88_512

A 3.5" floppy, with 2.88MB and 512 bytes/sector.

### -field F3_20Pt8_512

A 3.5" floppy, with 20.8MB and 512 bytes/sector.

### -field F3_720_512

A 3.5" floppy, with 720KB and 512 bytes/sector.

### -field F5_360_512

A 5.25" floppy, with 360KB and 512 bytes/sector.

### -field F5_320_512

A 5.25" floppy, with 320KB and 512 bytes/sector.

### -field F5_320_1024

A 5.25" floppy, with 320KB and 1024 bytes/sector.

### -field F5_180_512

A 5.25" floppy, with 180KB and 512 bytes/sector.

### -field F5_160_512

A 5.25" floppy, with 160KB and 512 bytes/sector.

### -field RemovableMedia

Removable media other than floppy.

### -field FixedMedia

Fixed hard disk media.

### -field F3_120M_512

A 3.5" floppy, with 120MB and 512 bytes/sector.

### -field F3_640_512

A 3.5" floppy, with 640KB and 512 bytes/sector.

### -field F5_640_512

A 5.25" floppy, with 640KB and 512 bytes/sector.

### -field F5_720_512

A 5.25" floppy, with 720KB and 512 bytes/sector.

### -field F3_1Pt2_512

A 3.5" floppy, with 1.2MB and 512 bytes/sector.

### -field F3_1Pt23_1024

A 3.5" floppy, with 1.23MB and 1024 bytes/sector.

### -field F5_1Pt23_1024

A 5.25" floppy, with 1.23MB and 1024 bytes/sector.

### -field F3_128Mb_512

A 3.5" floppy, with 128MB and 512 bytes/sector.

### -field F3_230Mb_512

A 3.5" floppy, with 230MB and 512 bytes/sector.

### -field F8_256_128

An 8" floppy, with 256KB and 128 bytes/sector.

### -field F3_200Mb_512

A 3.5" floppy, with 200MB and 512 bytes/sector. (HiFD).

### -field F3_240M_512

A 3.5" floppy, with 240MB and 512 bytes/sector. (HiFD).

### -field F3_32M_512

A 3.5" floppy, with 32MB and 512 bytes/sector.

## -remarks

The **MediaType** member of the [DISK_GEOMETRY](ns-winioctl-disk_geometry.md) data structure is of type **MEDIA_TYPE**. The [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) function receives a **DISK_GEOMETRY** structure in response to an [IOCTL_DISK_GET_DRIVE_GEOMETRY](ni-winioctl-ioctl_disk_get_drive_geometry.md) control code. The **DeviceIoControl** function receives an array of **DISK_GEOMETRY** structures in response to an [IOCTL_STORAGE_GET_MEDIA_TYPES](ni-winioctl-ioctl_storage_get_media_types.md) control code. The [STORAGE_MEDIA_TYPE](ne-winioctl-storage_media_type.md) enumeration type extends this enumeration type.

## -see-also

* [DISK_GEOMETRY](ns-winioctl-disk_geometry.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [IOCTL_DISK_GET_DRIVE_GEOMETRY](ni-winioctl-ioctl_disk_get_drive_geometry.md)
* [IOCTL_STORAGE_GET_MEDIA_TYPES](ni-winioctl-ioctl_storage_get_media_types.md)
* [STORAGE_MEDIA_TYPE](ne-winioctl-storage_media_type.md)

