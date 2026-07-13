---
UID: NE:virtdisk._RESIZE_VIRTUAL_DISK_VERSION
title: RESIZE_VIRTUAL_DISK_VERSION (virtdisk.h)
description: Enumerates the possible versions for parameters for the ResizeVirtualDisk function.
helpviewer_keywords: ["RESIZE_VIRTUAL_DISK_VERSION","RESIZE_VIRTUAL_DISK_VERSION enumeration [Virtual Storage]","RESIZE_VIRTUAL_DISK_VERSION_1","RESIZE_VIRTUAL_DISK_VERSION_UNSPECIFIED","virtdisk/RESIZE_VIRTUAL_DISK_VERSION","virtdisk/RESIZE_VIRTUAL_DISK_VERSION_1","virtdisk/RESIZE_VIRTUAL_DISK_VERSION_UNSPECIFIED","vstor.resize_virtual_disk_version"]
old-location: vstor\resize_virtual_disk_version.htm
tech.root: VStor
ms.assetid: 779381fb-4433-46c5-8caf-b830cd015c95
ms.date: 12/05/2018
ms.keywords: RESIZE_VIRTUAL_DISK_VERSION, RESIZE_VIRTUAL_DISK_VERSION enumeration [Virtual Storage], RESIZE_VIRTUAL_DISK_VERSION_1, RESIZE_VIRTUAL_DISK_VERSION_UNSPECIFIED, virtdisk/RESIZE_VIRTUAL_DISK_VERSION, virtdisk/RESIZE_VIRTUAL_DISK_VERSION_1, virtdisk/RESIZE_VIRTUAL_DISK_VERSION_UNSPECIFIED, vstor.resize_virtual_disk_version
req.header: virtdisk.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: RESIZE_VIRTUAL_DISK_VERSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RESIZE_VIRTUAL_DISK_VERSION
 - virtdisk/_RESIZE_VIRTUAL_DISK_VERSION
 - RESIZE_VIRTUAL_DISK_VERSION
 - virtdisk/RESIZE_VIRTUAL_DISK_VERSION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
api_name:
 - RESIZE_VIRTUAL_DISK_VERSION
---

# RESIZE_VIRTUAL_DISK_VERSION enumeration


## -description

Enumerates the possible versions for parameters for the 
    <a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk">ResizeVirtualDisk</a> function.

## -enum-fields

### -field RESIZE_VIRTUAL_DISK_VERSION_UNSPECIFIED:0

The version is not valid.

### -field RESIZE_VIRTUAL_DISK_VERSION_1:1

Version one of the parameters is used. This is the only supported value.

## -see-also

<a href="/windows/desktop/api/virtdisk/ns-virtdisk-resize_virtual_disk_parameters">RESIZE_VIRTUAL_DISK_PARAMETERS</a>



<a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk">ResizeVirtualDisk</a>



<a href="/previous-versions/windows/desktop/legacy/dd323698(v=vs.85)">VHD Enumerations</a>
