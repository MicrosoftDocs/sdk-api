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

# _MODIFY_VHDSET_PARAMETERS structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Contains VHD Set modification parameters, indicating how the VHD Set should be altered. 



## -struct-fields




### -field Version

A value from the MODIFY_VHDSET_VERSION enumeration that determines that is the discriminant for the union. 



### -field SnapshotPath

A structure with the following members.


### -field SnapshotPath.SnapshotId

The Snapshot Id in GUID format indicating which snapshot is to have its path altered in the VHD Set. 



### -field SnapshotPath.SnapshotFilePath

The new file path for the Snapshot indicated by the SnapshotId field. 



### -field SnapshotId

The Snapshot Id in GUID format indicating which snapshot is to be removed from the VHD Set file. 



### -field DefaultFilePath

The file path for the default Snapshot of the Vhd Set. 


