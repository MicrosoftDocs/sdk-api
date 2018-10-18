---
UID: NF:d2d1.ID2D1RenderTarget.DrawEllipse(const D2D1_ELLIPSE,ID2D1Brush,FLOAT,ID2D1StrokeStyle)
title: ID2D1RenderTarget::DrawEllipse(const D2D1_ELLIPSE,ID2D1Brush,FLOAT,ID2D1StrokeStyle)
author: windows-sdk-content
description: Draws the outline of the specified ellipse using the specified stroke style.
old-location: direct2d\ID2D1RenderTarget_DrawEllipse_ptr_D2D1_ELLIPSE_ptr_ID2D1Brush_FLOAT_ptr_ID2D1StrokeStyle.htm
tech.root: direct2d
ms.assetid: a760cc1e-4798-449d-bb45-693672d91132
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: DrawEllipse, DrawEllipse method [Direct2D], DrawEllipse method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],DrawEllipse method, ID2D1RenderTarget.DrawEllipse, ID2D1RenderTarget.DrawEllipse(const D2D1_ELLIPSE,ID2D1Brush,FLOAT,ID2D1StrokeStyle), ID2D1RenderTarget::DrawEllipse, ID2D1RenderTarget::DrawEllipse(const D2D1_ELLIPSE,ID2D1Brush,FLOAT,ID2D1StrokeStyle), d2d1/ID2D1RenderTarget::DrawEllipse, direct2d.ID2D1RenderTarget_DrawEllipse_ptr_D2D1_ELLIPSE_ptr_ID2D1Brush_FLOAT_ptr_ID2D1StrokeStyle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: 
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
req.lib: D2d1.lib
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
 - ID2D1RenderTarget.DrawEllipse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::DrawEllipse(const D2D1_ELLIPSE,ID2D1Brush,FLOAT,ID2D1StrokeStyle)


## -description


Draws the outline of the specified ellipse using the specified stroke style.


## -parameters




### -param ellipse [in]

Type: <b>const <a href="https://msdn.microsoft.com/6fed6c49-ba83-4c2b-af8a-04156ee317f0">D2D1_ELLIPSE</a>*</b>

The position and radius of the ellipse to draw, in device-independent pixels.


### -param brush [in]

Type: <b><a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>*</b>

The brush used to paint the ellipse's outline.


### -param strokeWidth

Type: <b>FLOAT</b>

The width of the stroke, in device-independent pixels. The value must be greater than or equal to 0.0f. If this parameter isn't specified, it defaults to 1.0f. The stroke is centered on the line.


### -param strokeStyle [in, optional]

Type: <b><a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a>*</b>

The style of stroke to apply to the ellipse's outline, or <b>NULL</b> to paint a solid stroke.


## -returns



This method does not return a value.




## -remarks



The <a href="https://msdn.microsoft.com/dabbb399-2d72-41c3-8b2f-aea49d7ad0cb">DrawEllipse</a> method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>DrawEllipse</b>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

