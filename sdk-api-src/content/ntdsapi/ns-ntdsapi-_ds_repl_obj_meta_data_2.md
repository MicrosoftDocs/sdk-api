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

# _DS_REPL_OBJ_META_DATA_2 structure


## -description


The <b>DS_REPL_OBJ_META_DATA_2</b> structure contains an array of <a href="https://msdn.microsoft.com/392457b7-df69-44d0-82b2-8381d5877354">DS_REPL_ATTR_META_DATA_2</a> structures, which in turn contain replication state data for the attributes (past and present) for a given object, as returned by the 
<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> function. This structure is an enhanced version of the <a href="https://msdn.microsoft.com/7851ffbc-5d05-4ea7-b3b4-1b8b77299be5">DS_REPL_OBJ_META_DATA</a> structure.


## -struct-fields




### -field cNumEntries

Contains the number of elements in the <b>rgMetaData</b> array.


### -field dwReserved

Not used.


### -field rgMetaData.size_is

 


### -field rgMetaData.size_is.cNumEntries

 


### -field rgMetaData

Contains an array of <a href="https://msdn.microsoft.com/392457b7-df69-44d0-82b2-8381d5877354">DS_REPL_ATTR_META_DATA_2</a> structures. The <b>cNumEntries</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/392457b7-df69-44d0-82b2-8381d5877354">DS_REPL_ATTR_META_DATA_2</a>



<a href="https://msdn.microsoft.com/7851ffbc-5d05-4ea7-b3b4-1b8b77299be5">DS_REPL_OBJ_META_DATA</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

