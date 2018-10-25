---
UID: NS:d2d1_1.D2D1_LAYER_PARAMETERS1
title: D2D1_LAYER_PARAMETERS1
author: windows-sdk-content
description: Contains the content bounds, mask information, opacity settings, and other options for a layer resource.
old-location: direct2d\d2d1_layer_parameters1.htm
tech.root: direct2d
ms.assetid: D7CC93F8-D871-4DFC-84A3-CA60EB52FF0A
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: D2D1_LAYER_PARAMETERS1, D2D1_LAYER_PARAMETERS1 structure [Direct2D], d2d1_1/D2D1_LAYER_PARAMETERS1, direct2d.d2d1_layer_parameters1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1_1.h
req.include-header: D2d1.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1_1.h
api_name:
 - D2D1_LAYER_PARAMETERS1
product: Windows
targetos: Windows
req.typenames: D2D1_LAYER_PARAMETERS1
req.redist: 
---

# D2D1_LAYER_PARAMETERS1 structure


## -description


Contains the content bounds, mask information, opacity settings, and other options for a layer resource.


## -struct-fields




### -field contentBounds

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a></b>

The content bounds of the layer. Content outside these bounds is not guaranteed to render.


### -field geometricMask

Type: <b><a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>*</b>

The geometric mask specifies the area of the layer that is composited into the render target. 


### -field maskAntialiasMode

Type: <b><a href="https://msdn.microsoft.com/3ca12155-6dd0-41bb-8778-3387422c4ffe">D2D1_ANTIALIAS_MODE</a></b>

A value that specifies the antialiasing mode for the geometricMask.  


### -field maskTransform

Type: <b><a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a></b>

A value that specifies the transform that is applied to the geometric mask when composing the layer.


### -field opacity

Type: <b>FLOAT</b>

An opacity value that is applied uniformly to all resources in the layer when compositing to the target.


### -field opacityBrush

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

A brush that is used to modify the opacity of the layer. The brush 
is mapped to the layer, and the alpha channel of each mapped brush pixel is multiplied against the corresponding layer pixel. 


### -field layerOptions

Type: <b><a href="https://msdn.microsoft.com/13C9EDE7-A1D0-4359-8EF3-77FF763B9244">D2D1_LAYER_OPTIONS1</a></b>

Additional options for the layer creation.


## -see-also




<a href="https://msdn.microsoft.com/22d161fb-8470-49cc-a523-309f90643ea9">Layers Overview</a>
 

 

