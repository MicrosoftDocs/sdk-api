---
UID: NF:gdiplusgraphics.Graphics.DrawImage(IN Image,IN RectF,IN Matrix,IN Effect,IN ImageAttributes,IN Unit)
title: Graphics::DrawImage(IN Image,IN RectF,IN Matrix,IN Effect,IN ImageAttributes,IN Unit) (gdiplusgraphics.h)
author: windows-sdk-content
description: The method draws a portion of an image after applying a specified effect.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_sourceRect_Matrix_xForm_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawimagemethods\drawimage_imageimage_rectfsourcerect_matrixxform.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrawImage, DrawImage method [GDI+], DrawImage method [GDI+],Graphics class, Graphics class [GDI+],DrawImage method, Graphics.DrawImage, Graphics.DrawImage(IN Image,IN RectF,IN Matrix,IN Effect,IN ImageAttributes,IN Unit), Graphics.DrawImage(Image*,RectF*,Matrix*,Effect*,ImageAttributes*,Unit*), Graphics::DrawImage, Graphics::DrawImage(IN Image,IN RectF,IN Matrix,IN Effect,IN ImageAttributes,IN Unit), _gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_sourceRect_Matrix_xForm_, gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_sourceRect_Matrix_xForm_
ms.topic: method
req.header: gdiplusgraphics.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Graphics.DrawImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::DrawImage(IN Image,IN RectF,IN Matrix,IN Effect,IN ImageAttributes,IN Unit)


## -description


The  method draws a portion of an image after applying a specified effect.


## -parameters




### -param image [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object that specifies the image to be drawn. 


### -param sourceRect [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a> object that specifies the portion of the image to be drawn.


### -param xForm [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a> object that specifies the parallelogram in which the image portion is rendered. The destination parallelogram is calculated by applying the affine transformation stored in the matrix to the source rectangle.


### -param effect [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534433(v=VS.85).aspx">Effect</a>*</b>

Pointer to a instance of a descendant of the <a href="https://msdn.microsoft.com/en-us/library/ms534433(v=VS.85).aspx">Effect</a> class. The descendant specifies an effect or adjustment (for example, a change in contrast) that is applied to the image before rendering. The image is not permanently altered by the effect.


### -param imageAttributes [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object that specifies color adjustments to be applied when the image is rendered. Can be <b>NULL</b>.


### -param srcUnit [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534405(v=VS.85).aspx">Unit</a>*</b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534405(v=VS.85).aspx">Unit</a> enumeration that specifies the unit of measure for the source rectangle.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536388(v=VS.85).aspx">Drawing, Positioning, and Cloning Images</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533830(v=VS.85).aspx">Loading and Displaying Bitmaps</a>
 

 

