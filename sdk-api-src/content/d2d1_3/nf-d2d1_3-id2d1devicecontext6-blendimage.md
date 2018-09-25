---
UID: NF:d2d1_3.ID2D1DeviceContext6.BlendImage
title: ID2D1DeviceContext6::BlendImage
author: windows-sdk-content
description: Draws an image to the device context using the specified blend mode. Results are equivalent to using Direct2D's built-in Blend effect.
old-location: direct2d\id2d1devicecontext6_blendimage.htm
tech.root: direct2d
ms.assetid: 598E98CA-3485-4188-84F0-DD711461AE44
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: BlendImage, BlendImage method [Direct2D], BlendImage method [Direct2D],ID2D1DeviceContext6 interface, ID2D1DeviceContext6 interface [Direct2D],BlendImage method, ID2D1DeviceContext6.BlendImage, ID2D1DeviceContext6::BlendImage, d2d1_3/ID2D1DeviceContext6::BlendImage, direct2d.id2d1devicecontext6_blendimage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext6.BlendImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext6::BlendImage


## -description


Draws an image to the device context using the specified blend mode. 
        Results are equivalent to using Direct2D's built-in <a href="https://msdn.microsoft.com/39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE">Blend effect</a>.


## -parameters




### -param image [in]

Type: <b>ID2D1Image*</b>

The image to be drawn to the device context.


### -param blendMode

Type: <b>D2D1_BLEND_MODE</b>

The blend mode to be used. See <a href="blend.htm">Blend modes</a> for more info.


### -param targetOffset [in, optional]

Type: <b>const D2D1_POINT_2F*</b>

The offset in the destination space that the image will be rendered to. 
            The entire logical extent of the image will be rendered to the corresponding destination. 
            If not specified, the destination origin will be (0, 0). 
            The top-left corner of the image will be mapped to the target offset. 
            This will not necessarily be the origin. The default value is NULL.


### -param imageRectangle [in, optional]

Type: <b>const D2D1_RECT_F*</b>

The corresponding rectangle in the image space will be mapped to the given origins when processing the image. The default value is NULL.


### -param interpolationMode

Type: <b>D2D1_INTERPOLATION_MODE</b>

The interpolation mode that will be used to scale the image if necessary. The default value is D2D1_INTERPOLATION_MODE_LINEAR.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/474788F4-8AD7-4D5C-BF0B-9542E69620A9">ID2D1DeviceContext6</a>
 

 

