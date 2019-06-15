---
UID: NE:fsrmenums._FsrmStorageModuleCaps
title: FsrmStorageModuleCaps (fsrmenums.h)
author: windows-sdk-content
description: Flags that define the capabilities of the storage module.
old-location: fsrm\fsrmstoragemodulecaps.htm
tech.root: fsrm
ms.assetid: 15d9bddc-fe6c-40c9-ba12-587c57c0bfcf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FsrmStorageModuleCaps, FsrmStorageModuleCaps enumeration [File Server Resource Manager], FsrmStorageModuleCaps_CanGet, FsrmStorageModuleCaps_CanHandleDirectories, FsrmStorageModuleCaps_CanHandleFiles, FsrmStorageModuleCaps_CanSet, FsrmStorageModuleCaps_Unknown, fs.fsrmstoragemodulecaps, fsrm.fsrmstoragemodulecaps, fsrmenums/FsrmStorageModuleCaps, fsrmenums/FsrmStorageModuleCaps_CanGet, fsrmenums/FsrmStorageModuleCaps_CanHandleDirectories, fsrmenums/FsrmStorageModuleCaps_CanHandleFiles, fsrmenums/FsrmStorageModuleCaps_CanSet, fsrmenums/FsrmStorageModuleCaps_Unknown
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmStorageModuleCaps
product: Windows
targetos: Windows
req.typenames: FsrmStorageModuleCaps
req.redist: 
ms.custom: 19H1
---

# FsrmStorageModuleCaps enumeration


## -description


Flags that define the capabilities of the storage module.


## -enum-fields




### -field FsrmStorageModuleCaps_Unknown

The storage module's capabilities are unknown. Do not use this value.


### -field FsrmStorageModuleCaps_CanGet

The storage module is allowed to retrieve classification properties.


### -field FsrmStorageModuleCaps_CanSet

The storage module is allowed to store classification properties.


### -field FsrmStorageModuleCaps_CanHandleDirectories

The storage module is allowed to handle folders. Only secure properties 
       (<b>FsrmPropertyDefinitionFlags_Secure</b> flags set on the 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertydefinition2-get_propertydefinitionflags">PropertyDefinitionFlags</a> 
       property) can be stored unless <b>FsrmStorageModuleCaps_CanHandleFiles</b> is also 
       specified.

<b>Windows Server 2008 R2:  </b>This storage module capability is not supported before Windows Server 2012.


### -field FsrmStorageModuleCaps_CanHandleFiles

The storage module is allowed to handle files.

<b>Windows Server 2008 R2:  </b>This storage module capability is not supported before Windows Server 2012.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmstoragemoduledefinition-get_capabilities">IFsrmStorageModuleDefinition.Capabilities</a>
 

 

