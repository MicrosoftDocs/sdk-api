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

# LayerParameters function


## -description


Creates a <a href="https://msdn.microsoft.com/ce575df6-9464-4672-9a0e-ff7e016d9354">D2D1_LAYER_PARAMETERS</a> structure.


## -parameters




### -param contentBounds [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a></b>

The content bounds of the layer. Content outside these bounds is not guaranteed to render.  The default value is <a href="https://msdn.microsoft.com/c2f75645-3197-4afa-81ac-8a362ce99620">D2D1::InfiniteRect</a>.


### -param geometricMask [in, optional]

Type: <b><a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>*</b>

A mask that specifies the area of the  layer that is composited into the render target, or <b>NULL</b>. The default value is <b>NULL</b>. 


### -param maskAntialiasMode

Type: <b><a href="https://msdn.microsoft.com/3ca12155-6dd0-41bb-8778-3387422c4ffe">D2D1_ANTIALIAS_MODE</a></b>

A value that specifies the antialiasing mode for the  geometric mask. The default value is   <a href="https://msdn.microsoft.com/3ca12155-6dd0-41bb-8778-3387422c4ffe">D2D1_ANTIALIAS_MODE_PER_PRIMITIVE</a>.


### -param maskTransform

Type: <b><a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a></b>

A value that specifies the transform that is applied to the geometric mask when composing the layer. The default value is <a href="https://msdn.microsoft.com/09c2ed59-db4a-4753-a98a-bef7748d3803">D2D1::IdentityMatrix</a>.


### -param opacity

Type: <b>FLOAT</b>

An opacity that is applied uniformly to all resources in the layer when compositing to the target. The default value is 1.0.


### -param opacityBrush

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

A brush that is used to alter the opacity of the layer. The brush 
is mapped to the layer, and the alpha channel of each mapped brush pixel is multiplied by the corresponding layer pixel.  The default value is <b>NULL</b>.


### -param layerOptions

Type: <b><a href="https://msdn.microsoft.com/d278211a-e99c-429d-9752-45c305f52ed8">D2D1_LAYER_OPTIONS</a></b>

A value that specifies whether the layer intends to render text with ClearType antialiasing. The default value is <a href="https://msdn.microsoft.com/d278211a-e99c-429d-9752-45c305f52ed8">D2D1_LAYER_OPTIONS_NONE</a>.



## -returns



Type: <b><a href="https://msdn.microsoft.com/ce575df6-9464-4672-9a0e-ff7e016d9354">D2D1_LAYER_PARAMETERS</a></b>

A structure that contains the content bounds, mask information, opacity settings, and other options for a layer resource.  




## -see-also




<a href="https://msdn.microsoft.com/3ca12155-6dd0-41bb-8778-3387422c4ffe">D2D1_ANTIALIAS_MODE</a>



<a href="https://msdn.microsoft.com/d278211a-e99c-429d-9752-45c305f52ed8">D2D1_LAYER_OPTIONS</a>



<a href="https://msdn.microsoft.com/ce575df6-9464-4672-9a0e-ff7e016d9354">D2D1_LAYER_PARAMETERS</a>



<a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>



<a href="https://msdn.microsoft.com/22d161fb-8470-49cc-a523-309f90643ea9">Layers Overview</a>
 

 

