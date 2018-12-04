---
UID: NF:d2d1_1.ID2D1CommandSink.DrawBitmap
title: ID2D1CommandSink::DrawBitmap
author: windows-sdk-content
description: Draws a bitmap to the render target.
old-location: direct2d\id2d1commandsink_drawbitmap.htm
tech.root: direct2d
ms.assetid: 95F73EBD-989E-4FB1-B1D2-86642E99FA3E
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: DrawBitmap, DrawBitmap method [Direct2D], DrawBitmap method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],DrawBitmap method, ID2D1CommandSink.DrawBitmap, ID2D1CommandSink::DrawBitmap, d2d1_1/ID2D1CommandSink::DrawBitmap, direct2d.id2d1commandsink_drawbitmap
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
 - ID2D1CommandSink.DrawBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink::DrawBitmap


## -description


Draws a bitmap to the render target.


## -parameters




### -param bitmap [in]

Type: <b><a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>*</b>

The bitmap to draw.


### -param destinationRectangle [in, optional]

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a></b>

The destination rectangle. The default is the size of the bitmap and the location is the upper left corner of the render target.


### -param opacity

Type: <b>FLOAT</b>

The opacity of the bitmap.


### -param interpolationMode

Type: <b><a href="https://msdn.microsoft.com/7a32f551-afad-4eb2-953f-a9acc71d7776">D2D1_INTERPOLATION_MODE</a></b>

The interpolation mode to use.


### -param sourceRectangle [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a></b>

An optional source rectangle.


### -param perspectiveTransform [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/6df02d4c-cd3c-697e-0aff-7f2d307d3d7d">D2D1_MATRIX_4X4_F</a></b>

An optional perspective transform.


## -returns



This method does not return a value.




## -remarks



The <i>destinationRectangle</i> parameter defines the rectangle in the target where the bitmap will appear (in device-independent pixels (DIPs)).  This is affected by the currently set transform and the perspective transform, if set.  If you specify NULL, then the destination rectangle is (left=0, top=0, right = width(<i>sourceRectangle</i>), bottom = height(<i>sourceRectangle</i>).



The <i>sourceRectangle</i> defines the sub-rectangle of the source bitmap (in DIPs).  <b>DrawBitmap</b> clips this rectangle to the size of the source bitmap, so it's impossible to sample outside of the bitmap.  If you specify NULL, then the source rectangle is taken to be the size of the source bitmap.



The <i>perspectiveTransform</i> is specified in addition to the transform on device context.





## -see-also




<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>
 

 

