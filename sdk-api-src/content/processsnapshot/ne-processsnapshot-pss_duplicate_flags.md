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

# PSS_DUPLICATE_FLAGS enumeration


## -description


Duplication flags for use by <a href="https://msdn.microsoft.com/5D2751F3-E7E1-4917-8060-E2BC8A7A3DEA">PssDuplicateSnapshot</a>.


## -enum-fields




### -field PSS_DUPLICATE_NONE

No flag.


### -field PSS_DUPLICATE_CLOSE_SOURCE

Free the source handle. This will only succeed if you set the  <b>PSS_CREATE_USE_VM_ALLOCATIONS</b> flag when you called <a href="https://msdn.microsoft.com/44F2CB48-A9F6-4131-B21C-9F27A27CECD5">PssCaptureSnapshot</a> to create the snapshot and handle. The handle will be freed  even if duplication fails.
The close operation does not protect against concurrent access to the same descriptor.


## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

