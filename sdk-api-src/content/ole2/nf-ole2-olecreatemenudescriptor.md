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

# OleCreateMenuDescriptor function


## -description


Creates and returns an OLE menu descriptor (that is, an OLE-provided data structure that describes the menus) for OLE to use when dispatching menu messages and commands.


## -parameters




### -param hmenuCombined [in]

Handle to the combined menu created by the object.


### -param lpMenuWidths [in]

Pointer to an array of six <b>LONG</b> values giving the number of menus in each group.


## -returns



Returns the handle to the descriptor, or <b>NULL</b> if insufficient memory is available.





## -remarks



The <b>OleCreateMenuDescriptor</b> function can be called by the object to create a descriptor for the composite menu. OLE then uses this descriptor to dispatch menu messages and commands. To free the shared menu descriptor when it is no longer needed, the container should call the companion helper function, <a href="https://msdn.microsoft.com/dc347d39-a7bb-4bbf-8957-c3fbcff461bf">OleDestroyMenuDescriptor</a>.





## -see-also




<a href="https://msdn.microsoft.com/dc347d39-a7bb-4bbf-8957-c3fbcff461bf">OleDestroyMenuDescriptor</a>
 

 

