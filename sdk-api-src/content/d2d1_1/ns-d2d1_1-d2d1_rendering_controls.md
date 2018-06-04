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

# D2D1_RENDERING_CONTROLS structure


## -description


Describes limitations to be applied to an imaging effect renderer.


## -struct-fields




### -field bufferPrecision

The buffer precision used by default if the buffer precision is not otherwise specified by the effect or the transform.


### -field tileSize

The tile allocation size to be used by the imaging effect renderer.


## -remarks



The renderer can allocate tiles larger than the minimum tile allocation. The allocated tiles will be powers of two of the minimum size on each axis, except that the size on each axis will not exceed the guaranteed maximum texture size for the device feature level. 

The <b>minimumPixelRenderExtent</b> is the size of the square tile below which the renderer will expand the tile allocation rather than attempting to subdivide the rendering tile any further. When this threshold is reached, the allocation tile size is expanded. This might occur repeatedly until rendering can either proceed or it is determined that the graph cannot be rendered.

The buffer precision is used for intermediate buffers if it is otherwise unspecified by the effects or the internal effect topology. The application can also use the <a href="https://msdn.microsoft.com/6a59c903-0fa8-4d2c-b426-8d3c3410c6bd">Output.BufferPrecision</a> method to specify the output precision for a particular effect. This takes precedence over the context precision. In addition, the effect might set a different precision internally if required. If the buffer type on the context is <b>D2D1_BUFFER_PRECISION_UNKNOWN</b> and otherwise not specified by the effect or transform, the precision of the output will be the maximum precision of the inputs to the transform. The buffer precision does not affect the number of channels used. 




## -see-also




<a href="https://msdn.microsoft.com/6a066126-89d0-4372-bc01-6b6fa1d65440">ID2D1DeviceContext::SetRenderingControls</a>
 

 

