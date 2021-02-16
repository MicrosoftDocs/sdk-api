---
UID: NS:virtdisk._EXPAND_VIRTUAL_DISK_PARAMETERS
title: EXPAND_VIRTUAL_DISK_PARAMETERS (virtdisk.h)
description: Contains virtual disk expansion request parameters.
helpviewer_keywords: ["*PEXPAND_VIRTUAL_DISK_PARAMETERS","EXPAND_VIRTUAL_DISK_PARAMETERS","EXPAND_VIRTUAL_DISK_PARAMETERS structure [VHD]","PEXPAND_VIRTUAL_DISK_PARAMETERS","PEXPAND_VIRTUAL_DISK_PARAMETERS structure pointer [VHD]","_EXPAND_VIRTUAL_DISK_PARAMETERS","vdssys/EXPAND_VIRTUAL_DISK_PARAMETERS","vdssys/PEXPAND_VIRTUAL_DISK_PARAMETERS","vhd.expand_virtual_disk_parameters","virtdisk/EXPAND_VIRTUAL_DISK_PARAMETERS","virtdisk/PEXPAND_VIRTUAL_DISK_PARAMETERS"]
old-location: vhd\expand_virtual_disk_parameters.htm
tech.root: VStor
ms.assetid: 8a8a4d1c-7dbc-4dfe-9f21-94a3370553b8
ms.date: 12/05/2018
ms.keywords: '*PEXPAND_VIRTUAL_DISK_PARAMETERS, EXPAND_VIRTUAL_DISK_PARAMETERS, EXPAND_VIRTUAL_DISK_PARAMETERS structure [VHD], PEXPAND_VIRTUAL_DISK_PARAMETERS, PEXPAND_VIRTUAL_DISK_PARAMETERS structure pointer [VHD], _EXPAND_VIRTUAL_DISK_PARAMETERS, vdssys/EXPAND_VIRTUAL_DISK_PARAMETERS, vdssys/PEXPAND_VIRTUAL_DISK_PARAMETERS, vhd.expand_virtual_disk_parameters, virtdisk/EXPAND_VIRTUAL_DISK_PARAMETERS, virtdisk/PEXPAND_VIRTUAL_DISK_PARAMETERS'
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
req.typenames: EXPAND_VIRTUAL_DISK_PARAMETERS, *PEXPAND_VIRTUAL_DISK_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EXPAND_VIRTUAL_DISK_PARAMETERS
 - virtdisk/_EXPAND_VIRTUAL_DISK_PARAMETERS
 - PEXPAND_VIRTUAL_DISK_PARAMETERS
 - virtdisk/PEXPAND_VIRTUAL_DISK_PARAMETERS
 - EXPAND_VIRTUAL_DISK_PARAMETERS
 - virtdisk/EXPAND_VIRTUAL_DISK_PARAMETERS
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
 - EXPAND_VIRTUAL_DISK_PARAMETERS
---

# EXPAND_VIRTUAL_DISK_PARAMETERS structure


## -description

Contains virtual disk expansion request parameters.

## -struct-fields

### -field Version

An <a href="/windows/win32/api/virtdisk/ne-virtdisk-expand_virtual_disk_version">EXPAND_VIRTUAL_DISK_VERSION</a> 
      enumeration value that specifies the version of the 
      <b>EXPAND_VIRTUAL_DISK_PARAMETERS</b> structure 
      being passed to or from the virtual disk functions.

### -field Version1

This structure is used if the <b>Version</b> member is 
       <b>EXPAND_VIRTUAL_DISK_VERSION_1</b> (1).

### -field Version1.NewSize

New size, in bytes, for the expansion request.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>