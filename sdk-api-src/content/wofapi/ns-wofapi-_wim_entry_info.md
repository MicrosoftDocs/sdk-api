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

# _WIM_ENTRY_INFO structure


## -description


Defines metadata specific to each WIM data source hosted on a volume.


## -struct-fields




### -field WimEntryInfoSize

Specifies the size of the structure.  Should be initialized to sizeof(WIM_ENTRY_INFO).


### -field WimType

Specifies the type of the WIM.  Valid values are WIM_BOOT_OS_WIM and zero, which implies the WIM is not an operating system WIM.


### -field DataSourceId

Specifies a unique identifier for this data source.


### -field WimGuid

Specifies the GUID which is stored in the WIM file’s header.


### -field WimPath

Specifies a full path to the WIM file.


### -field WimIndex

Specifies the index within the WIM which is described by this data source.


### -field Flags

Specifies one or more flags for this data source.  Can include WIM_ENTRY_FLAG_NOT_ACTIVE, indicating a data source which is removed or where the WIM file is not found, or WIM_ENTRY_FLAG_SUSPENDED indicating that the data source is not currently in use but could become in use on demand.  If neither flag is present, the WIM is in active use.

