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

# IDirectManipulationViewport::SetViewportTransform


## -description


Specifies the transform from the viewport coordinate system to the window client coordinate system. 


## -parameters




### -param matrix [in]

The transform matrix, in row-wise order: _11, _12, _21, _22, _31, _32.


### -param pointCount [in]

The size of the transform matrix. This value is always 6, because a 3x2 matrix is used for all direct manipulation transforms.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Call this function to specify the viewport position, scaling and orientation on the screen. Viewport position, scaling, orientation and size are uniquely determined by the viewport transform and the viewport rectangle. The application can specify the viewport transform using this method, and the viewport rectangle using <a href="https://msdn.microsoft.com/45dfdf6e-aa4d-489a-bf9a-016e42eb57f6">SetViewportRect</a>. 


The viewport rectangle (the rectangular area inside the content that is visible to the user) is specified in viewport coordinates. If the viewport rectangle top-left point is (0,0), the viewport rectangle is positioned exactly at the viewport coordinate system origin. Viewports offset from the viewport coordinate system origin can be specified in two ways:

<ul>
<li>Through the viewport rectangle top-left point</li>
<li>Through the viewport transform translation component (_31, _32)</li>
</ul>
The viewport transform converts from the viewport coordinate system to the window client coordinate system. <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> ignores the window RTL property, so the client area origin is always the top-left point. 
The transforms are applied in the following order:


<ol>
<li>Viewport rectangle offset</li>
<li>Viewport transform (from viewport to client coordinate system)</li>
<li>Client to screen mapping (from client to screen coordinate system)
</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

