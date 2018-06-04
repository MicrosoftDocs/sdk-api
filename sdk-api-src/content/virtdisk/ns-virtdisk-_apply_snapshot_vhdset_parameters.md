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

# _APPLY_SNAPSHOT_VHDSET_PARAMETERS structure


## -description


Contains snapshot parameters, indicating information about the new snapshot to be applied. 


## -struct-fields




### -field Version

An <a href="https://msdn.microsoft.com/3146B123-5118-495E-A640-11026DAD84C4">APPLY_SNAPSHOT_VHDSET_VERSION</a> 
     enumeration that specifies the version of the 
     <b>APPLY_SNAPSHOT_VHDSET_PARAMETERS</b> structure being passed to or from the VHD functions.


### -field Version1

A structure with the following member.


### -field Version1.SnapshotId

The ID of the new snapshot to be applied to the VHD set. 


### -field Version1.LeafSnapshotId

Indicates whether the current default leaf data should be retained as part of the apply operation. When a zero GUID is specified, the apply operation will discard the current default leaf data. When a non-zero GUID is specified, the apply operation will convert the default leaf data into a writeable snapshot with the specified ID. 


