---
UID: NS:virtdisk._STORAGE_DEPENDENCY_INFO_TYPE_1
title: STORAGE_DEPENDENCY_INFO_TYPE_1 (virtdisk.h)
description: Contains virtual hard disk (VHD) storage dependency information for type 1.
helpviewer_keywords: ["*PSTORAGE_DEPENDENCY_INFO_TYPE_1","PSTORAGE_DEPENDENCY_INFO_TYPE_1","PSTORAGE_DEPENDENCY_INFO_TYPE_1 structure pointer [VHD]","STORAGE_DEPENDENCY_INFO_TYPE_1","STORAGE_DEPENDENCY_INFO_TYPE_1 structure [VHD]","_STORAGE_DEPENDENCY_INFO_TYPE_1","vdssys/PSTORAGE_DEPENDENCY_INFO_TYPE_1","vdssys/STORAGE_DEPENDENCY_INFO_TYPE_1","vhd.storage_dependency_info_type_1","virtdisk/PSTORAGE_DEPENDENCY_INFO_TYPE_1","virtdisk/STORAGE_DEPENDENCY_INFO_TYPE_1"]
old-location: vhd\storage_dependency_info_type_1.htm
tech.root: VStor
ms.assetid: 63296975-583d-415c-8c1f-f0cccfc5a1b3
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_DEPENDENCY_INFO_TYPE_1, PSTORAGE_DEPENDENCY_INFO_TYPE_1, PSTORAGE_DEPENDENCY_INFO_TYPE_1 structure pointer [VHD], STORAGE_DEPENDENCY_INFO_TYPE_1, STORAGE_DEPENDENCY_INFO_TYPE_1 structure [VHD], _STORAGE_DEPENDENCY_INFO_TYPE_1, vdssys/PSTORAGE_DEPENDENCY_INFO_TYPE_1, vdssys/STORAGE_DEPENDENCY_INFO_TYPE_1, vhd.storage_dependency_info_type_1, virtdisk/PSTORAGE_DEPENDENCY_INFO_TYPE_1, virtdisk/STORAGE_DEPENDENCY_INFO_TYPE_1'
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
req.typenames: STORAGE_DEPENDENCY_INFO_TYPE_1, *PSTORAGE_DEPENDENCY_INFO_TYPE_1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _STORAGE_DEPENDENCY_INFO_TYPE_1
 - virtdisk/_STORAGE_DEPENDENCY_INFO_TYPE_1
 - PSTORAGE_DEPENDENCY_INFO_TYPE_1
 - virtdisk/PSTORAGE_DEPENDENCY_INFO_TYPE_1
 - STORAGE_DEPENDENCY_INFO_TYPE_1
 - virtdisk/STORAGE_DEPENDENCY_INFO_TYPE_1
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
 - STORAGE_DEPENDENCY_INFO_TYPE_1
---

# STORAGE_DEPENDENCY_INFO_TYPE_1 structure


## -description

Contains virtual hard disk (VHD) storage dependency information for type 1.

## -struct-fields

### -field DependencyTypeFlags

A <a href="/windows/win32/api/virtdisk/ne-virtdisk-dependent_disk_flag">DEPENDENT_DISK_FLAG</a> enumeration.

### -field ProviderSpecificFlags

Flags specific to the VHD provider.

### -field VirtualStorageType

A <a href="/windows/win32/api/virtdisk/ns-virtdisk-virtual_storage_type">VIRTUAL_STORAGE_TYPE</a> structure.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>