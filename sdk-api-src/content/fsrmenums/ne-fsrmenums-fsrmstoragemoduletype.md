---
UID: NE:fsrmenums._FsrmStorageModuleType
title: FsrmStorageModuleType (fsrmenums.h)
description: Defines the possible storage module types.
helpviewer_keywords: ["FsrmStorageModuleType","FsrmStorageModuleType enumeration [File Server Resource Manager]","FsrmStorageModuleType_Cache","FsrmStorageModuleType_Database","FsrmStorageModuleType_InFile","FsrmStorageModuleType_System","FsrmStorageModuleType_Unknown","fs.fsrmstoragemoduletype","fsrm.fsrmstoragemoduletype","fsrmenums/FsrmStorageModuleType","fsrmenums/FsrmStorageModuleType_Cache","fsrmenums/FsrmStorageModuleType_Database","fsrmenums/FsrmStorageModuleType_InFile","fsrmenums/FsrmStorageModuleType_System","fsrmenums/FsrmStorageModuleType_Unknown"]
old-location: fsrm\fsrmstoragemoduletype.htm
tech.root: fsrm
ms.assetid: 7cd1d4eb-de69-44d2-89f9-41e1e9a371e0
ms.date: 12/05/2018
ms.keywords: FsrmStorageModuleType, FsrmStorageModuleType enumeration [File Server Resource Manager], FsrmStorageModuleType_Cache, FsrmStorageModuleType_Database, FsrmStorageModuleType_InFile, FsrmStorageModuleType_System, FsrmStorageModuleType_Unknown, fs.fsrmstoragemoduletype, fsrm.fsrmstoragemoduletype, fsrmenums/FsrmStorageModuleType, fsrmenums/FsrmStorageModuleType_Cache, fsrmenums/FsrmStorageModuleType_Database, fsrmenums/FsrmStorageModuleType_InFile, fsrmenums/FsrmStorageModuleType_System, fsrmenums/FsrmStorageModuleType_Unknown
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: FsrmStorageModuleType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmStorageModuleType
 - fsrmenums/_FsrmStorageModuleType
 - FsrmStorageModuleType
 - fsrmenums/FsrmStorageModuleType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmStorageModuleType
---

# FsrmStorageModuleType enumeration


## -description

Defines the possible storage module types.

## -enum-fields

### -field FsrmStorageModuleType_Unknown:0

The module type is unknown. Do not use this value.

### -field FsrmStorageModuleType_Cache:1

The storage module caches classification properties for quick access. This type is reserved for use by FSRM 
      and should not be used by any third party providers.

### -field FsrmStorageModuleType_InFile:2

The storage module stores classification properties within the file itself.

### -field FsrmStorageModuleType_Database:3

The storage module stores classification properties in a database.

### -field FsrmStorageModuleType_System:100

The storage module stores classification properties in system data store. This type is reserved for use by 
       FSRM and should not be used by any third party providers.

<b>Windows Server 2008 R2:  </b>This storage module type is not supported before Windows Server 2012.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-enumerations">FSRM Enumerations</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmstoragemoduledefinition-get_storagetype">IFsrmStorageModuleDefinition.StorageType</a>
