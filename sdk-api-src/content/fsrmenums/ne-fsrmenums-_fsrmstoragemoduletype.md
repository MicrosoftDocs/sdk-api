---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

