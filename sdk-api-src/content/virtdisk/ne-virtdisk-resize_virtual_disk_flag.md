---
UID: NE:virtdisk._RESIZE_VIRTUAL_DISK_FLAG
title: RESIZE_VIRTUAL_DISK_FLAG (virtdisk.h)
description: Enumerates the available flags for the ResizeVirtualDisk function.
helpviewer_keywords: ["RESIZE_VIRTUAL_DISK_FLAG","RESIZE_VIRTUAL_DISK_FLAG enumeration [Virtual Storage]","RESIZE_VIRTUAL_DISK_FLAG_ALLOW_UNSAFE_VIRTUAL_SIZE","RESIZE_VIRTUAL_DISK_FLAG_NONE","RESIZE_VIRTUAL_DISK_FLAG_RESIZE_TO_SMALLEST_SAFE_VIRTUAL_SIZE","virtdisk/RESIZE_VIRTUAL_DISK_FLAG","virtdisk/RESIZE_VIRTUAL_DISK_FLAG_ALLOW_UNSAFE_VIRTUAL_SIZE","virtdisk/RESIZE_VIRTUAL_DISK_FLAG_NONE","virtdisk/RESIZE_VIRTUAL_DISK_FLAG_RESIZE_TO_SMALLEST_SAFE_VIRTUAL_SIZE","vstor.resize_virtual_disk_flag"]
old-location: vstor\resize_virtual_disk_flag.htm
tech.root: VStor
ms.assetid: dd4fc68d-8bed-47ce-94a2-a8a71199fac2
ms.date: 12/05/2018
ms.keywords: RESIZE_VIRTUAL_DISK_FLAG, RESIZE_VIRTUAL_DISK_FLAG enumeration [Virtual Storage], RESIZE_VIRTUAL_DISK_FLAG_ALLOW_UNSAFE_VIRTUAL_SIZE, RESIZE_VIRTUAL_DISK_FLAG_NONE, RESIZE_VIRTUAL_DISK_FLAG_RESIZE_TO_SMALLEST_SAFE_VIRTUAL_SIZE, virtdisk/RESIZE_VIRTUAL_DISK_FLAG, virtdisk/RESIZE_VIRTUAL_DISK_FLAG_ALLOW_UNSAFE_VIRTUAL_SIZE, virtdisk/RESIZE_VIRTUAL_DISK_FLAG_NONE, virtdisk/RESIZE_VIRTUAL_DISK_FLAG_RESIZE_TO_SMALLEST_SAFE_VIRTUAL_SIZE, vstor.resize_virtual_disk_flag
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
req.typenames: RESIZE_VIRTUAL_DISK_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RESIZE_VIRTUAL_DISK_FLAG
 - virtdisk/_RESIZE_VIRTUAL_DISK_FLAG
 - RESIZE_VIRTUAL_DISK_FLAG
 - virtdisk/RESIZE_VIRTUAL_DISK_FLAG
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
 - RESIZE_VIRTUAL_DISK_FLAG
---

# RESIZE_VIRTUAL_DISK_FLAG enumeration


## -description

Enumerates the available flags for the 
    <a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk">ResizeVirtualDisk</a> function.

## -enum-fields

### -field RESIZE_VIRTUAL_DISK_FLAG_NONE:0x0

No flags are specified.

### -field RESIZE_VIRTUAL_DISK_FLAG_ALLOW_UNSAFE_VIRTUAL_SIZE:0x1

If this flag is set, skip checking the virtual disk's partition table to ensure that this truncation is 
      safe. Setting this flag can cause unrecoverable data loss; use with care.

### -field RESIZE_VIRTUAL_DISK_FLAG_RESIZE_TO_SMALLEST_SAFE_VIRTUAL_SIZE:0x2

If this flag is set, resize the disk to the smallest virtual size possible without truncating past any 
      existing partitions. If this is set, the <b>NewSize</b> member in the 
      <a href="/windows/desktop/api/virtdisk/ns-virtdisk-resize_virtual_disk_parameters">RESIZE_VIRTUAL_DISK_PARAMETERS</a> 
      structure must be zero.

## -see-also

<a href="/windows/desktop/api/virtdisk/ns-virtdisk-resize_virtual_disk_parameters">RESIZE_VIRTUAL_DISK_PARAMETERS</a>



<a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk">ResizeVirtualDisk</a>



<a href="/previous-versions/windows/desktop/legacy/dd323698(v=vs.85)">VHD Enumerations</a>
