---
UID: NS:virtdisk._MIRROR_VIRTUAL_DISK_PARAMETERS
title: MIRROR_VIRTUAL_DISK_PARAMETERS (virtdisk.h)
description: Contains virtual hard disk (VHD) mirror request parameters.
helpviewer_keywords: ["*PMIRROR_VIRTUAL_DISK_PARAMETERS","MIRROR_VIRTUAL_DISK_PARAMETERS","MIRROR_VIRTUAL_DISK_PARAMETERS structure [VHD]","PMIRROR_VIRTUAL_DISK_PARAMETERS","PMIRROR_VIRTUAL_DISK_PARAMETERS structure pointer [VHD]","_MIRROR_VIRTUAL_DISK_PARAMETERS","vdssys/MIRROR_VIRTUAL_DISK_PARAMETERS","vdssys/PMIRROR_VIRTUAL_DISK_PARAMETERS","vhd.mirror_virtual_disk_parameters","virtdisk/MIRROR_VIRTUAL_DISK_PARAMETERS","virtdisk/PMIRROR_VIRTUAL_DISK_PARAMETERS"]
old-location: vhd\mirror_virtual_disk_parameters.htm
tech.root: VStor
ms.assetid: bcde890e-24d5-41ac-8e5a-ba0d99e395e1
ms.date: 12/05/2018
ms.keywords: '*PMIRROR_VIRTUAL_DISK_PARAMETERS, MIRROR_VIRTUAL_DISK_PARAMETERS, MIRROR_VIRTUAL_DISK_PARAMETERS structure [VHD], PMIRROR_VIRTUAL_DISK_PARAMETERS, PMIRROR_VIRTUAL_DISK_PARAMETERS structure pointer [VHD], _MIRROR_VIRTUAL_DISK_PARAMETERS, vdssys/MIRROR_VIRTUAL_DISK_PARAMETERS, vdssys/PMIRROR_VIRTUAL_DISK_PARAMETERS, vhd.mirror_virtual_disk_parameters, virtdisk/MIRROR_VIRTUAL_DISK_PARAMETERS, virtdisk/PMIRROR_VIRTUAL_DISK_PARAMETERS'
req.header: virtdisk.h
req.include-header: 
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
req.typenames: MIRROR_VIRTUAL_DISK_PARAMETERS, *PMIRROR_VIRTUAL_DISK_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIRROR_VIRTUAL_DISK_PARAMETERS
 - virtdisk/_MIRROR_VIRTUAL_DISK_PARAMETERS
 - PMIRROR_VIRTUAL_DISK_PARAMETERS
 - virtdisk/PMIRROR_VIRTUAL_DISK_PARAMETERS
 - MIRROR_VIRTUAL_DISK_PARAMETERS
 - virtdisk/MIRROR_VIRTUAL_DISK_PARAMETERS
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
 - MIRROR_VIRTUAL_DISK_PARAMETERS
---

# MIRROR_VIRTUAL_DISK_PARAMETERS structure


## -description

Contains virtual hard disk (VHD) mirror request parameters.

## -struct-fields

### -field Version

Indicates the version of this structure to use. Set this to 
      <b>MIRROR_VIRTUAL_DISK_VERSION_1</b> (1).

### -field Version1

This structure is used if the <b>Version</b> member is set to 
       <b>MIRROR_VIRTUAL_DISK_VERSION_1</b>.

### -field Version1.MirrorVirtualDiskPath

<a href="/windows/desktop/FileIO/naming-a-file">Fully qualified</a> path where the mirrored 
         virtual disk will be located. If the <i>Flags</i> parameter to 
         <a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk">MirrorVirtualDisk</a> is 
         <b>MIRROR_VIRTUAL_DISK_FLAG_NONE</b> (0) then this file must not exist. If the 
         <i>Flags</i> parameter to 
         <b>MirrorVirtualDisk</b> is 
         <b>MIRROR_VIRTUAL_DISK_FLAG_EXISTING_FILE</b> (1) then this file must exist.

## -see-also

<a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk">MirrorVirtualDisk</a>



<a href="/previous-versions/windows/desktop/legacy/dd323699(v=vs.85)">VHD Functions</a>