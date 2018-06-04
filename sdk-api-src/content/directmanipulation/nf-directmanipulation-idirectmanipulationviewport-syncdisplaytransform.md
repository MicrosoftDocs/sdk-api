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

# IDirectManipulationViewport::SyncDisplayTransform


## -description


Specifies a display transform for the viewport, and synchronizes the output transform with the new value of the display transform.


## -parameters




### -param matrix [in]

The transform matrix, in row-wise order: _11, _12, _21, _22, _31, _32.


### -param pointCount [in]

The size of the transform matrix. This value is always 6, because a 3x2 matrix is used for all direct manipulation transforms.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



If the application performs special output processing of the content outside of the compositor (content not fully captured in the viewport transform), it should call this method to specify the display transform for the special processing.


The display transform affects how manipulation updates are applied to the output transform. For example, if the display transform is set to scale 3x, panning will move the content 3x the original distance. 


When a display transform is changed using this method, the output transform will be synchronized to the new value of the display transform.


This method cannot be called if the viewport status is <b>DIRECTMANIPULATION_RUNNING</b> or <b>DIRECTMANIPULATION_INERTIA</b>.





## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

