---
UID: NS:virtdisk._STORAGE_DEPENDENCY_INFO
title: STORAGE_DEPENDENCY_INFO (virtdisk.h)
description: Contains virtual hard disk (VHD) storage dependency information.
helpviewer_keywords: ["*PSTORAGE_DEPENDENCY_INFO","PSTORAGE_DEPENDENCY_INFO","PSTORAGE_DEPENDENCY_INFO structure pointer [VHD]","STORAGE_DEPENDENCY_INFO","STORAGE_DEPENDENCY_INFO structure [VHD]","_STORAGE_DEPENDENCY_INFO","vdssys/PSTORAGE_DEPENDENCY_INFO","vdssys/STORAGE_DEPENDENCY_INFO","vhd.storage_dependency_info","virtdisk/PSTORAGE_DEPENDENCY_INFO","virtdisk/STORAGE_DEPENDENCY_INFO"]
old-location: vhd\storage_dependency_info.htm
tech.root: VStor
ms.assetid: 67648a4d-3f66-407e-9036-c7072bc7e460
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_DEPENDENCY_INFO, PSTORAGE_DEPENDENCY_INFO, PSTORAGE_DEPENDENCY_INFO structure pointer [VHD], STORAGE_DEPENDENCY_INFO, STORAGE_DEPENDENCY_INFO structure [VHD], _STORAGE_DEPENDENCY_INFO, vdssys/PSTORAGE_DEPENDENCY_INFO, vdssys/STORAGE_DEPENDENCY_INFO, vhd.storage_dependency_info, virtdisk/PSTORAGE_DEPENDENCY_INFO, virtdisk/STORAGE_DEPENDENCY_INFO'
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
req.typenames: STORAGE_DEPENDENCY_INFO, *PSTORAGE_DEPENDENCY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _STORAGE_DEPENDENCY_INFO
 - virtdisk/_STORAGE_DEPENDENCY_INFO
 - PSTORAGE_DEPENDENCY_INFO
 - virtdisk/PSTORAGE_DEPENDENCY_INFO
 - STORAGE_DEPENDENCY_INFO
 - virtdisk/STORAGE_DEPENDENCY_INFO
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
 - STORAGE_DEPENDENCY_INFO
---

# STORAGE_DEPENDENCY_INFO structure


## -description

Contains virtual hard disk (VHD) storage dependency information.

## -struct-fields

### -field Version

A [STORAGE_DEPENDENCY_INFO_TYPE_1](./ns-virtdisk-storage_dependency_info_type_1.md) or [STORAGE_DEPENDENCY_INFO_TYPE_2](./ns-virtdisk-storage_dependency_info_type_2.md).

### -field NumberEntries

Number of entries returned in the following unioned members.

### -field Version1Entries

Variable-length array containing <a href="/windows/win32/api/virtdisk/ns-virtdisk-storage_dependency_info_type_1">STORAGE_DEPENDENCY_INFO_TYPE_1</a> structures.

### -field Version2Entries

Variable-length array containing <a href="/windows/win32/api/virtdisk/ns-virtdisk-storage_dependency_info_type_2">STORAGE_DEPENDENCY_INFO_TYPE_2</a> structures.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>