---
UID: NS:virtdisk._STORAGE_DEPENDENCY_INFO_TYPE_2
title: STORAGE_DEPENDENCY_INFO_TYPE_2 (virtdisk.h)
description: Contains VHD or ISO storage dependency information for type 2.
helpviewer_keywords: ["*PSTORAGE_DEPENDENCY_INFO_TYPE_2","PSTORAGE_DEPENDENCY_INFO_TYPE_2","PSTORAGE_DEPENDENCY_INFO_TYPE_2 structure pointer [VHD]","STORAGE_DEPENDENCY_INFO_TYPE_2","STORAGE_DEPENDENCY_INFO_TYPE_2 structure [VHD]","_STORAGE_DEPENDENCY_INFO_TYPE_2","vdssys/PSTORAGE_DEPENDENCY_INFO_TYPE_2","vdssys/STORAGE_DEPENDENCY_INFO_TYPE_2","vhd.storage_dependency_info_type_2","virtdisk/PSTORAGE_DEPENDENCY_INFO_TYPE_2","virtdisk/STORAGE_DEPENDENCY_INFO_TYPE_2"]
old-location: vhd\storage_dependency_info_type_2.htm
tech.root: VStor
ms.assetid: f3e57773-0008-4715-9136-a9b990beea58
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_DEPENDENCY_INFO_TYPE_2, PSTORAGE_DEPENDENCY_INFO_TYPE_2, PSTORAGE_DEPENDENCY_INFO_TYPE_2 structure pointer [VHD], STORAGE_DEPENDENCY_INFO_TYPE_2, STORAGE_DEPENDENCY_INFO_TYPE_2 structure [VHD], _STORAGE_DEPENDENCY_INFO_TYPE_2, vdssys/PSTORAGE_DEPENDENCY_INFO_TYPE_2, vdssys/STORAGE_DEPENDENCY_INFO_TYPE_2, vhd.storage_dependency_info_type_2, virtdisk/PSTORAGE_DEPENDENCY_INFO_TYPE_2, virtdisk/STORAGE_DEPENDENCY_INFO_TYPE_2'
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
req.typenames: STORAGE_DEPENDENCY_INFO_TYPE_2, *PSTORAGE_DEPENDENCY_INFO_TYPE_2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _STORAGE_DEPENDENCY_INFO_TYPE_2
 - virtdisk/_STORAGE_DEPENDENCY_INFO_TYPE_2
 - PSTORAGE_DEPENDENCY_INFO_TYPE_2
 - virtdisk/PSTORAGE_DEPENDENCY_INFO_TYPE_2
 - STORAGE_DEPENDENCY_INFO_TYPE_2
 - virtdisk/STORAGE_DEPENDENCY_INFO_TYPE_2
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
 - STORAGE_DEPENDENCY_INFO_TYPE_2
---

# STORAGE_DEPENDENCY_INFO_TYPE_2 structure


## -description

Contains VHD or ISO storage dependency information for type 2.

## -struct-fields

### -field DependencyTypeFlags

A <a href="/windows/win32/api/virtdisk/ne-virtdisk-dependent_disk_flag">DEPENDENT_DISK_FLAG</a> enumeration.

### -field ProviderSpecificFlags

Flags specific to the VHD provider.

### -field VirtualStorageType

A <a href="/windows/win32/api/virtdisk/ns-virtdisk-virtual_storage_type">VIRTUAL_STORAGE_TYPE</a> structure.

### -field AncestorLevel

The ancestor level.

### -field DependencyDeviceName

The device name of the dependent device. If the device is a virtual hard drive then this will be in the 
      form \\.\PhysicalDrive<i>N</i>. If the device is a virtual CD or DVD drive 
      (ISO) then this will be in the form \\.\CDRom<i>N</i>. In either case 
      <i>N</i> is an integer that represents a unique identifier for the caller's host 
      system.

### -field HostVolumeName

The host disk volume name in the form \\?\Volume{<i>GUID</i>}\ where 
      <i>GUID</i> is the <b>GUID</b> that identifies the volume.

### -field DependentVolumeName

The name of the dependent volume, if any, in the form 
      \\?\Volume{<i>GUID</i>}\ where <i>GUID</i> is the 
      <b>GUID</b> that identifies the volume.

### -field DependentVolumeRelativePath

The relative path to the dependent volume.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>