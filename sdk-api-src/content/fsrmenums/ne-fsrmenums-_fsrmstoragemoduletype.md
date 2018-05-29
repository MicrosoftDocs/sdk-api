---
UID: NE:fsrmenums._FsrmStorageModuleType
title: "_FsrmStorageModuleType"
author: windows-sdk-content
description: Defines the possible storage module types.
old-location: fsrm\fsrmstoragemoduletype.htm
old-project: Fsrm
ms.assetid: 7cd1d4eb-de69-44d2-89f9-41e1e9a371e0
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: FsrmStorageModuleType, FsrmStorageModuleType enumeration [File Server Resource Manager], FsrmStorageModuleType_Cache, FsrmStorageModuleType_Database, FsrmStorageModuleType_InFile, FsrmStorageModuleType_System, FsrmStorageModuleType_Unknown, _FsrmStorageModuleType, fs.fsrmstoragemoduletype, fsrm.fsrmstoragemoduletype, fsrmenums/FsrmStorageModuleType, fsrmenums/FsrmStorageModuleType_Cache, fsrmenums/FsrmStorageModuleType_Database, fsrmenums/FsrmStorageModuleType_InFile, fsrmenums/FsrmStorageModuleType_System, fsrmenums/FsrmStorageModuleType_Unknown
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: FsrmStorageModuleType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	FsrmEnums.h
api_name:
-	FsrmStorageModuleType
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# _FsrmStorageModuleType enumeration


## -description


Defines the possible storage module types.


## -enum-fields




### -field FsrmStorageModuleType_Unknown

The module type is unknown. Do not use this value.


### -field FsrmStorageModuleType_Cache

The storage module caches classification properties for quick access. This type is reserved for use by FSRM 
      and should not be used by any third party providers.


### -field FsrmStorageModuleType_InFile

The storage module stores classification properties within the file itself.


### -field FsrmStorageModuleType_Database

The storage module stores classification properties in a database.


### -field FsrmStorageModuleType_System

The storage module stores classification properties in system data store. This type is reserved for use by 
       FSRM and should not be used by any third party providers.

<b>Windows Server 2008 R2:  </b>This storage module type is not supported before Windows Server 2012.


## -see-also




<a href="https://msdn.microsoft.com/93fdf667-8959-40a9-a374-c54ed73bbe89">FSRM Enumerations</a>



<a href="https://msdn.microsoft.com/4c4aaacf-d121-412c-9152-5787f351c19c">IFsrmStorageModuleDefinition.StorageType</a>
 

 

