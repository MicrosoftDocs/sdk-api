---
UID: NS:virtdisk._RESIZE_VIRTUAL_DISK_PARAMETERS
title: RESIZE_VIRTUAL_DISK_PARAMETERS (virtdisk.h)
description: Contains the parameters for a ResizeVirtualDisk function.
helpviewer_keywords: ["*PRESIZE_VIRTUAL_DISK_PARAMETERS","PRESIZE_VIRTUAL_DISK_PARAMETERS","PRESIZE_VIRTUAL_DISK_PARAMETERS structure pointer [Virtual Storage]","RESIZE_VIRTUAL_DISK_PARAMETERS","RESIZE_VIRTUAL_DISK_PARAMETERS structure [Virtual Storage]","_RESIZE_VIRTUAL_DISK_PARAMETERS","virtdisk/PRESIZE_VIRTUAL_DISK_PARAMETERS","virtdisk/RESIZE_VIRTUAL_DISK_PARAMETERS","vstor.resize_virtual_disk_parameters"]
old-location: vstor\resize_virtual_disk_parameters.htm
tech.root: VStor
ms.assetid: ff44f07a-67d1-4ad3-be2b-0aea1d3c4a6a
ms.date: 12/05/2018
ms.keywords: '*PRESIZE_VIRTUAL_DISK_PARAMETERS, PRESIZE_VIRTUAL_DISK_PARAMETERS, PRESIZE_VIRTUAL_DISK_PARAMETERS structure pointer [Virtual Storage], RESIZE_VIRTUAL_DISK_PARAMETERS, RESIZE_VIRTUAL_DISK_PARAMETERS structure [Virtual Storage], _RESIZE_VIRTUAL_DISK_PARAMETERS, virtdisk/PRESIZE_VIRTUAL_DISK_PARAMETERS, virtdisk/RESIZE_VIRTUAL_DISK_PARAMETERS, vstor.resize_virtual_disk_parameters'
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
req.typenames: RESIZE_VIRTUAL_DISK_PARAMETERS, *PRESIZE_VIRTUAL_DISK_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RESIZE_VIRTUAL_DISK_PARAMETERS
 - virtdisk/_RESIZE_VIRTUAL_DISK_PARAMETERS
 - PRESIZE_VIRTUAL_DISK_PARAMETERS
 - virtdisk/PRESIZE_VIRTUAL_DISK_PARAMETERS
 - RESIZE_VIRTUAL_DISK_PARAMETERS
 - virtdisk/RESIZE_VIRTUAL_DISK_PARAMETERS
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
 - RESIZE_VIRTUAL_DISK_PARAMETERS
---

# RESIZE_VIRTUAL_DISK_PARAMETERS structure


## -description

Contains the parameters for a 
    <a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk">ResizeVirtualDisk</a> function.

## -struct-fields

### -field Version

Discriminant for the union containing a value enumerated from the 
      <a href="/windows/desktop/api/virtdisk/ne-virtdisk-resize_virtual_disk_version">RESIZE_VIRTUAL_DISK_VERSION</a> 
      enumeration.

### -field Version1

If the <b>Version</b> member is 
       <b>RESIZE_VIRTUAL_DISK_VERSION_1</b> (1), this structure is used.

### -field Version1.NewSize

Contains the new size of the virtual disk.

## -see-also

<a href="/windows/desktop/api/virtdisk/ne-virtdisk-resize_virtual_disk_version">RESIZE_VIRTUAL_DISK_VERSION</a>



<a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk">ResizeVirtualDisk</a>



<a href="/previous-versions/windows/desktop/legacy/dd323699(v=vs.85)">VHD Functions</a>