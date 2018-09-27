---
UID: NF:d2d1_1.ID2D1DeviceContext.DrawImage(ID2D1Image,D2D1_POINT_2F,D2D1_INTERPOLATION_MODE,D2D1_COMPOSITE_MODE)
title: ID2D1DeviceContext::DrawImage(ID2D1Image,D2D1_POINT_2F,D2D1_INTERPOLATION_MODE,D2D1_COMPOSITE_MODE)
author: windows-sdk-content
description: Draws an image to the device context.
old-location: direct2d\id2d1devicecontext_drawimage.htm
tech.root: direct2d
ms.assetid: c41d8a79-280a-451e-b07b-f904d07da5c7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DrawImage, DrawImage method [Direct2D], DrawImage method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],DrawImage method, ID2D1DeviceContext.DrawImage, ID2D1DeviceContext.DrawImage(ID2D1Image,D2D1_POINT_2F,D2D1_INTERPOLATION_MODE,D2D1_COMPOSITE_MODE), ID2D1DeviceContext::DrawImage, ID2D1DeviceContext::DrawImage(ID2D1Image,D2D1_POINT_2F,D2D1_INTERPOLATION_MODE,D2D1_COMPOSITE_MODE), d2d1_1/ID2D1DeviceContext::DrawImage, direct2d.id2d1devicecontext_drawimage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID2D1DeviceContext.DrawImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::DrawImage(ID2D1Image,D2D1_POINT_2F,D2D1_INTERPOLATION_MODE,D2D1_COMPOSITE_MODE)


## -description


Draws an image to the device context.


## -parameters




#### - image [in]

Type: <b><a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>*</b>

The image to be drawn to the device context.


#### - targetOffset [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

The  offset in the destination space that the image will be rendered to. The entire logical extent of the image will be rendered to the corresponding destination. If not specified, the destination origin will be (0, 0). The top-left corner of the image will be mapped to the target offset. This will not necessarily be the origin. This default value is <i>NULL</i>.


### -param interpolationMode

Type: <b><a href="direct2d.__D2D1_INTERPOLATION_MODE">D2D1_INTERPOLATION_MODE</a></b>

The interpolation mode that will be used to scale the image if necessary.


### -param compositeMode

Type: <b><a href="https://msdn.microsoft.com/4f01e805-aed7-4bfc-9793-42a9fdde3473">D2D1_COMPOSITE_MODE</a></b>

The composite mode that will be applied to the limits of the currently selected clip. The default value is <b>D2D1_COMPOSITE_MODE_SOURCE_OVER</b>


#### - imageRectangle [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The corresponding rectangle in the image space will be mapped to the given origins when processing the image. This default value is <i>NULL</i>.


## -returns



This method does not return a value.




## -remarks



If <i>interpolationMode</i> is <b>D2D1_INTERPOLATION_MODE_HIGH_QUALITY</b>, different scalers will be used depending on the scale factor implied by the world transform.

Any invalid rectangles accumulated on any effect that is drawn by this call will be discarded regardless of which portion of the image rectangle is drawn.

If <i>compositeMode</i> is <b>D2D1_COMPOSITE_MODE_SOURCE_OVER</b>, <b>DrawImage</b> will use the currently selected primitive blend specified by <a href="https://msdn.microsoft.com/be04c9f7-397f-468e-91c0-3b11c68b489f">ID2D1DeviceContext::SetPrimitiveBlend</a>. If <i>compositeMode</i> is not <b>D2D1_COMPOSITE_MODE_SOURCE_OVER</b>, the image will be extended to transparent up to the current axis-aligned clip.

If there is an image rectangle and a world transform, this is equivalent to inserting a clip effect to represent the image rectangle and a 2D affine transform to take into account the world transform.




## -see-also




<a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>



<a href="https://msdn.microsoft.com/669a9377-248c-4a86-b447-ed117fff43a6">ID2D1Bitmap1</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>



<a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a>



<a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>
 

 

