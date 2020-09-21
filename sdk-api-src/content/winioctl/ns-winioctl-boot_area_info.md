---
UID: NS:winioctl._BOOT_AREA_INFO
title: BOOT_AREA_INFO
description: Contains the output for the FSCTL_GET_BOOT_AREA_INFO control code.
helpviewer_keywords: ["*PBOOT_AREA_INFO","BOOT_AREA_INFO","BOOT_AREA_INFO structure [Files]","PBOOT_AREA_INFO","PBOOT_AREA_INFO structure pointer [Files]","fs.boot_area_info","winioctl/BOOT_AREA_INFO","winioctl/PBOOT_AREA_INFO"]
old-location: fs\boot_area_info.htm
tech.root: fs
ms.assetid: e6ec156d-6a20-4b00-89fb-a27421fffbc0
ms.date: 12/05/2018
ms.keywords: '*PBOOT_AREA_INFO, BOOT_AREA_INFO, BOOT_AREA_INFO structure [Files], PBOOT_AREA_INFO, PBOOT_AREA_INFO structure pointer [Files], fs.boot_area_info, winioctl/BOOT_AREA_INFO, winioctl/PBOOT_AREA_INFO'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: BOOT_AREA_INFO, *PBOOT_AREA_INFO
req.redist: 
f1_keywords:
 - _BOOT_AREA_INFO
 - winioctl/_BOOT_AREA_INFO
 - PBOOT_AREA_INFO
 - winioctl/PBOOT_AREA_INFO
 - BOOT_AREA_INFO
 - winioctl/BOOT_AREA_INFO
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
 - BOOT_AREA_INFO
---

# BOOT_AREA_INFO structure


## -description

Contains the output for the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_boot_area_info">FSCTL_GET_BOOT_AREA_INFO</a> control code.

## -struct-fields

### -field BootSectorCount

Number of elements in the <b>BootSectors</b> array.

### -field Offset

### -field BootSectors

A variable length array of structures each containing the following member.



#### Offset

The location of a boot sector or a copy of a boot sector.

## -syntax

```cpp
typedef struct _BOOT_AREA_INFO {
  DWORD                    BootSectorCount;
  struct {
    LARGE_INTEGER Offset;
  } BootSectors[2];
} BOOT_AREA_INFO, *PBOOT_AREA_INFO;
```

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_boot_area_info">FSCTL_GET_BOOT_AREA_INFO</a>