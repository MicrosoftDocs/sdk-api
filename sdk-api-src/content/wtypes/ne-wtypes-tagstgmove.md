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

# tagSTGMOVE enumeration


## -description



			The 
<b>STGMOVE</b> enumeration values indicate whether a storage element is to be moved or copied. They are used in the 
<a href="https://msdn.microsoft.com/d9d33c64-edac-480f-b295-b2a06e51af2e">IStorage::MoveElementTo</a> method.


## -enum-fields




### -field STGMOVE_MOVE

Indicates that the method should move the data from the source to the destination.


### -field STGMOVE_COPY

Indicates that the method should copy the data from the source to the destination. A copy is the same as a move except that the source element is not removed after copying the element to the destination. Copying an element on top of itself is undefined.


### -field STGMOVE_SHALLOWCOPY

Not implemented.


## -see-also




<a href="https://msdn.microsoft.com/d9d33c64-edac-480f-b295-b2a06e51af2e">IStorage::MoveElementTo</a>
 

 

