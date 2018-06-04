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

# DCOMPOSITION_BACKFACE_VISIBILITY enumeration


## -description


Specifies the backface visibility to be applied to a visual.  


## -enum-fields




### -field DCOMPOSITION_BACKFACE_VISIBILITY_VISIBLE

Surfaces in this visual's sub-tree are visible regardless of transformation.


### -field DCOMPOSITION_BACKFACE_VISIBILITY_HIDDEN

Surfaces in this visual's sub-tree are only visible when facing the observer.


### -field DCOMPOSITION_BACKFACE_VISIBILITY_INHERIT

The back face visibility is the same as that of the target visual's parent visual.


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=313910">DirectComposition Backface and D2D Batching</a>



<a href="https://msdn.microsoft.com/A488A0B9-3CBE-477A-9688-84A7DA43D7F6">IDCompositionVisual2::SetBackFaceVisibility</a>



<b>Sample</b>
 

 

