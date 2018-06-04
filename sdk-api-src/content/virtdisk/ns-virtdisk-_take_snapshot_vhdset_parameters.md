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

# _TAKE_SNAPSHOT_VHDSET_PARAMETERS structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Contains snapshot parameters, indicating information about the new snapshot to be created. 



## -struct-fields




### -field Version

A value from the <a href="https://msdn.microsoft.com/E544AC22-6865-4ECF-92F8-B8027746C231">TAKE_SNAPSHOT_VHDSET_VERSION</a> enumeration that is the discriminant for the union. 



### -field Version1

A structure with the following member.


### -field Version1.SnapshotId

The Id of the new Snapshot to be added to the Vhd Set. 


