---
UID: NS:winioctl._FILE_STORAGE_TIER
title: FILE_STORAGE_TIER
description: Represents an identifier for the storage tier relative to the volume.
helpviewer_keywords: ["*PFILE_STORAGE_TIER","FILE_STORAGE_TIER","FILE_STORAGE_TIER structure [Files]","FILE_STORAGE_TIER_FLAG_NO_SEEK_PENALTY","PFILE_STORAGE_TIER","PFILE_STORAGE_TIER structure pointer [Files]","fs.file_storage_tier","winioctl/FILE_STORAGE_TIER","winioctl/PFILE_STORAGE_TIER"]
old-location: fs\file_storage_tier.htm
tech.root: fs
ms.assetid: F9701D3B-57B3-4777-841C-3D45A2CEC17E
ms.date: 12/05/2018
ms.keywords: '*PFILE_STORAGE_TIER, FILE_STORAGE_TIER, FILE_STORAGE_TIER structure [Files], FILE_STORAGE_TIER_FLAG_NO_SEEK_PENALTY, PFILE_STORAGE_TIER, PFILE_STORAGE_TIER structure pointer [Files], fs.file_storage_tier, winioctl/FILE_STORAGE_TIER, winioctl/PFILE_STORAGE_TIER'
req.header: winioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
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
req.typenames: FILE_STORAGE_TIER, *PFILE_STORAGE_TIER
req.redist: 
f1_keywords:
 - _FILE_STORAGE_TIER
 - winioctl/_FILE_STORAGE_TIER
 - PFILE_STORAGE_TIER
 - winioctl/PFILE_STORAGE_TIER
 - FILE_STORAGE_TIER
 - winioctl/FILE_STORAGE_TIER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoctl.h
api_name:
 - FILE_STORAGE_TIER
---

# FILE_STORAGE_TIER structure


## -description

Represents an identifier for the storage tier relative to the volume.

## -struct-fields

### -field Id

Tier ID.

### -field Name

Name for the tier.

### -field Description

Note for the tier.

### -field Flags

The file storage tier flags. This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_STORAGE_TIER_FLAG_NO_SEEK_PENALTY"></a><a id="file_storage_tier_flag_no_seek_penalty"></a><dl>
<dt><b>FILE_STORAGE_TIER_FLAG_NO_SEEK_PENALTY</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Tier does not suffer a seek penalty on IO operations, which indicates that is an SSD (solid state drive).

</td>
</tr>
</table>

### -field ProvisionedCapacity

Provisioned capacity of the tier.

### -field MediaType

Media type of the tier.

### -field Class

## -remarks

The storage tier ID for a particular volume has no relationship to the storage tier ID with the same value on a different volume.

