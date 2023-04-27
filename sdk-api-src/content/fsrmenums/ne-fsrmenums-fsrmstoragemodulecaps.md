---
UID: NE:fsrmenums._FsrmStorageModuleCaps
title: FsrmStorageModuleCaps (fsrmenums.h)
description: Flags that define the capabilities of the storage module.
helpviewer_keywords: ["FsrmStorageModuleCaps","FsrmStorageModuleCaps enumeration [File Server Resource Manager]","FsrmStorageModuleCaps_CanGet","FsrmStorageModuleCaps_CanHandleDirectories","FsrmStorageModuleCaps_CanHandleFiles","FsrmStorageModuleCaps_CanSet","FsrmStorageModuleCaps_Unknown","fs.fsrmstoragemodulecaps","fsrm.fsrmstoragemodulecaps","fsrmenums/FsrmStorageModuleCaps","fsrmenums/FsrmStorageModuleCaps_CanGet","fsrmenums/FsrmStorageModuleCaps_CanHandleDirectories","fsrmenums/FsrmStorageModuleCaps_CanHandleFiles","fsrmenums/FsrmStorageModuleCaps_CanSet","fsrmenums/FsrmStorageModuleCaps_Unknown"]
old-location: fsrm\fsrmstoragemodulecaps.htm
tech.root: fsrm
ms.assetid: 15d9bddc-fe6c-40c9-ba12-587c57c0bfcf
ms.date: 12/05/2018
ms.keywords: FsrmStorageModuleCaps, FsrmStorageModuleCaps enumeration [File Server Resource Manager], FsrmStorageModuleCaps_CanGet, FsrmStorageModuleCaps_CanHandleDirectories, FsrmStorageModuleCaps_CanHandleFiles, FsrmStorageModuleCaps_CanSet, FsrmStorageModuleCaps_Unknown, fs.fsrmstoragemodulecaps, fsrm.fsrmstoragemodulecaps, fsrmenums/FsrmStorageModuleCaps, fsrmenums/FsrmStorageModuleCaps_CanGet, fsrmenums/FsrmStorageModuleCaps_CanHandleDirectories, fsrmenums/FsrmStorageModuleCaps_CanHandleFiles, fsrmenums/FsrmStorageModuleCaps_CanSet, fsrmenums/FsrmStorageModuleCaps_Unknown
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmEnums.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FsrmStorageModuleCaps
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmStorageModuleCaps
 - fsrmenums/_FsrmStorageModuleCaps
 - FsrmStorageModuleCaps
 - fsrmenums/FsrmStorageModuleCaps
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
 - FsrmStorageModuleCaps
---

# FsrmStorageModuleCaps enumeration


## -description

Flags that define the capabilities of the storage module.

## -enum-fields

### -field FsrmStorageModuleCaps_Unknown:0

The storage module's capabilities are unknown. Do not use this value.

### -field FsrmStorageModuleCaps_CanGet:0x1

The storage module is allowed to retrieve classification properties.

### -field FsrmStorageModuleCaps_CanSet:0x2

The storage module is allowed to store classification properties.

### -field FsrmStorageModuleCaps_CanHandleDirectories:0x4

The storage module is allowed to handle folders. Only secure properties 
       (<b>FsrmPropertyDefinitionFlags_Secure</b> flags set on the 
       <a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertydefinition2-get_propertydefinitionflags">PropertyDefinitionFlags</a> 
       property) can be stored unless <b>FsrmStorageModuleCaps_CanHandleFiles</b> is also 
       specified.

<b>Windows Server 2008 R2:  </b>This storage module capability is not supported before Windows Server 2012.

### -field FsrmStorageModuleCaps_CanHandleFiles:0x8

The storage module is allowed to handle files.

<b>Windows Server 2008 R2:  </b>This storage module capability is not supported before Windows Server 2012.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmstoragemoduledefinition-get_capabilities">IFsrmStorageModuleDefinition.Capabilities</a>
