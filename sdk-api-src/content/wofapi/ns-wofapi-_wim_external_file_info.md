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

# _WIM_EXTERNAL_FILE_INFO structure


## -description


Defines metadata specific to files provided by WOF_PROVIDER_WIM.


## -struct-fields




### -field DataSourceId

Specifies the data source from which the file’s data is being provided.


### -field ResourceHash

 


### -field Flags

Specifies one or more flags for this data file.  When creating a new backed file, this member should be zero.  When querying the state of an existing file, this member can include WIM_ENTRY_FLAG_NOT_ACTIVE, indicating the data source is removed or the WIM file is not found, or WIM_ENTRY_FLAG_SUSPENDED indicating that the data source is not currently in use but could become in use on demand.


#### - ResourceHash[WIM_PROVIDER_HASH_SIZE]

Specifies the identifier of the file within the WIM file.

