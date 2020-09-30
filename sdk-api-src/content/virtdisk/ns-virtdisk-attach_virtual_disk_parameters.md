---
UID: NS:virtdisk._ATTACH_VIRTUAL_DISK_PARAMETERS
title: ATTACH_VIRTUAL_DISK_PARAMETERS (virtdisk.h)
description: Contains virtual hard disk (VHD) attach request parameters.
helpviewer_keywords: ["*PATTACH_VIRTUAL_DISK_PARAMETERS","ATTACH_VIRTUAL_DISK_PARAMETERS","ATTACH_VIRTUAL_DISK_PARAMETERS structure [VHD]","PATTACH_VIRTUAL_DISK_PARAMETERS","PATTACH_VIRTUAL_DISK_PARAMETERS structure pointer [VHD]","_ATTACH_VIRTUAL_DISK_PARAMETERS","vdssys/ATTACH_VIRTUAL_DISK_PARAMETERS","vdssys/PATTACH_VIRTUAL_DISK_PARAMETERS","vhd.attach_virtual_disk_parameters","vhd.surface_virtual_disk_parameters","virtdisk/ATTACH_VIRTUAL_DISK_PARAMETERS","virtdisk/PATTACH_VIRTUAL_DISK_PARAMETERS"]
old-location: vhd\attach_virtual_disk_parameters.htm
tech.root: VStor
ms.assetid: 2bccad87-ddfe-4db4-9bf3-1892d8dd1237
ms.date: 12/05/2018
ms.keywords: '*PATTACH_VIRTUAL_DISK_PARAMETERS, ATTACH_VIRTUAL_DISK_PARAMETERS, ATTACH_VIRTUAL_DISK_PARAMETERS structure [VHD], PATTACH_VIRTUAL_DISK_PARAMETERS, PATTACH_VIRTUAL_DISK_PARAMETERS structure pointer [VHD], _ATTACH_VIRTUAL_DISK_PARAMETERS, vdssys/ATTACH_VIRTUAL_DISK_PARAMETERS, vdssys/PATTACH_VIRTUAL_DISK_PARAMETERS, vhd.attach_virtual_disk_parameters, vhd.surface_virtual_disk_parameters, virtdisk/ATTACH_VIRTUAL_DISK_PARAMETERS, virtdisk/PATTACH_VIRTUAL_DISK_PARAMETERS'
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: ATTACH_VIRTUAL_DISK_PARAMETERS, *PATTACH_VIRTUAL_DISK_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ATTACH_VIRTUAL_DISK_PARAMETERS
 - virtdisk/_ATTACH_VIRTUAL_DISK_PARAMETERS
 - PATTACH_VIRTUAL_DISK_PARAMETERS
 - virtdisk/PATTACH_VIRTUAL_DISK_PARAMETERS
 - ATTACH_VIRTUAL_DISK_PARAMETERS
 - virtdisk/ATTACH_VIRTUAL_DISK_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
 - vdssys.h
api_name:
 - ATTACH_VIRTUAL_DISK_PARAMETERS
---

# ATTACH_VIRTUAL_DISK_PARAMETERS structure


## -description

Contains virtual hard disk (VHD)  attach request parameters.

## -struct-fields

### -field Version

A <a href="/windows/win32/api/virtdisk/ne-virtdisk-attach_virtual_disk_version">ATTACH_VIRTUAL_DISK_VERSION</a> 
     enumeration that specifies the version of the 
     <b>ATTACH_VIRTUAL_DISK_PARAMETERS</b> 
     structure being passed to or from the VHD functions.

### -field Version1

A structure with the following member.

### -field Version1.Reserved

Reserved.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>