---
UID: NF:d2d1.ID2D1RenderTarget.DrawBitmap(ID2D1Bitmap,const D2D1_RECT_F &,FLOAT,D2D1_BITMAP_INTERPOLATION_MODE,const D2D1_RECT_F &)
title: ID2D1RenderTarget::DrawBitmap(ID2D1Bitmap,const D2D1_RECT_F &,FLOAT,D2D1_BITMAP_INTERPOLATION_MODE,const D2D1_RECT_F &)
author: windows-sdk-content
description: Draws the specified bitmap after scaling it to the size of the specified rectangle.
old-location: direct2d\ID2D1RenderTarget_DrawBitmap_ptr_ID2D1Bitmap_ref_D2D_RECT_F_FLOAT_D2D1_BITMAP_INTERPOLATION_MODE_ref_D2D_RECT_F.htm
tech.root: direct2d
ms.assetid: 7a02772f-dc7a-4fc3-8695-a29810fb080b
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: DrawBitmap, DrawBitmap method [Direct2D], DrawBitmap method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],DrawBitmap method, ID2D1RenderTarget.DrawBitmap, ID2D1RenderTarget.DrawBitmap(ID2D1Bitmap,const D2D1_RECT_F &,FLOAT,D2D1_BITMAP_INTERPOLATION_MODE,const D2D1_RECT_F &), ID2D1RenderTarget::DrawBitmap, ID2D1RenderTarget::DrawBitmap(ID2D1Bitmap,const D2D1_RECT_F &,FLOAT,D2D1_BITMAP_INTERPOLATION_MODE,const D2D1_RECT_F &), d2d1/ID2D1RenderTarget::DrawBitmap, direct2d.ID2D1RenderTarget_DrawBitmap_ptr_ID2D1Bitmap_ref_D2D_RECT_F_FLOAT_D2D1_BITMAP_INTERPOLATION_MODE_ref_D2D_RECT_F
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
 - ID2D1RenderTarget.DrawBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::DrawBitmap(ID2D1Bitmap,const D2D1_RECT_F &,FLOAT,D2D1_BITMAP_INTERPOLATION_MODE,const D2D1_RECT_F &)


## -description


Draws the specified bitmap after scaling it to the size of the specified rectangle.


## -parameters




### -param bitmap [in]

Type: <b><a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>*</b>

The bitmap to render.


### -param destinationRectangle [ref]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a></b>

The size and position, in device-independent pixels in the render target's coordinate space, of the area to which the bitmap is drawn. If the rectangle is not well-ordered, nothing is drawn, but the render target does not enter an error state.


### -param opacity

Type: <b>FLOAT</b>

A value between 0.0f and 1.0f, inclusive, that specifies an opacity value to apply to the bitmap; this value is multiplied against the alpha values of the bitmap's contents.  


### -param interpolationMode

Type: <b><a href="https://msdn.microsoft.com/b53b7e0a-aa8b-4788-896c-9825c9e6cceb">D2D1_BITMAP_INTERPOLATION_MODE</a></b>

The interpolation mode to use if the bitmap is scaled or rotated by the drawing operation. 


### -param sourceRectangle [ref]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a></b>

The size and position, in device-independent pixels in the bitmap's coordinate space, of the area within the bitmap to draw.


## -returns



This method does not return a value.




## -remarks



This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <a href="https://msdn.microsoft.com/241df698-ca5e-4d94-902a-a9e140820c14">DrawBitmap</a>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

