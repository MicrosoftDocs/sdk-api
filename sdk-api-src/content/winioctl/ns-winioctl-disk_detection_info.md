---
UID: NS:winioctl._DISK_DETECTION_INFO
title: DISK_DETECTION_INFO
description: Contains detected drive parameters.
helpviewer_keywords: ["*PDISK_DETECTION_INFO","DISK_DETECTION_INFO","DISK_DETECTION_INFO structure [Files]","DetectExInt13","DetectInt13","DetectNone","PDISK_DETECTION_INFO","PDISK_DETECTION_INFO structure pointer [Files]","_win32_disk_detection_info_str","base.disk_detection_info_str","fs.disk_detection_info_str","winioctl/DISK_DETECTION_INFO","winioctl/PDISK_DETECTION_INFO"]
old-location: fs\disk_detection_info_str.htm
tech.root: fs
ms.assetid: 57ca68f4-f748-4bc4-90c3-13d545716d87
ms.date: 12/05/2018
ms.keywords: '*PDISK_DETECTION_INFO, DISK_DETECTION_INFO, DISK_DETECTION_INFO structure [Files], DetectExInt13, DetectInt13, DetectNone, PDISK_DETECTION_INFO, PDISK_DETECTION_INFO structure pointer [Files], _win32_disk_detection_info_str, base.disk_detection_info_str, fs.disk_detection_info_str, winioctl/DISK_DETECTION_INFO, winioctl/PDISK_DETECTION_INFO'
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
req.typenames: DISK_DETECTION_INFO, *PDISK_DETECTION_INFO
req.redist: 
f1_keywords:
 - _DISK_DETECTION_INFO
 - winioctl/_DISK_DETECTION_INFO
 - PDISK_DETECTION_INFO
 - winioctl/PDISK_DETECTION_INFO
 - DISK_DETECTION_INFO
 - winioctl/DISK_DETECTION_INFO
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
 - DISK_DETECTION_INFO
---

# DISK_DETECTION_INFO structure


## -description

Contains detected drive parameters.

## -struct-fields

### -field SizeOfDetectInfo

The size of the structure, in bytes.

### -field DetectionType

The detected partition type.

This member can be one of the following values from the **DETECTION_TYPE** enumeration.

| Value | Enumeration | Meaning |
| --- | --- | --- |
| **DetectExInt13** | 2 | The disk has an extended Int13 partition. |
| **DetectInt13** | 1 | The disk has a standard Int13 partition. |
| **DetectNone** | 0 | The disk does not have an Int13 or an extended Int13 partition. |

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Int13

If **DetectionType** is DetectInt13, the union is a [**DISK_INT13_INFO**](ns-winioctl-disk_int13_info.md) structure.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ExInt13

If **DetectionType** is DetectExInt13, the union is a [**DISK_EX_INT13_INFO**](ns-winioctl-disk_ex_int13_info.md) structure.

## -see-also

[DISK_EX_INT13_INFO](ns-winioctl-disk_ex_int13_info.md), [DISK_INT13_INFO](ns-winioctl-disk_int13_info.md), [DISK_GEOMETRY_EX](ns-winioctl-disk_geometry_ex.md)

