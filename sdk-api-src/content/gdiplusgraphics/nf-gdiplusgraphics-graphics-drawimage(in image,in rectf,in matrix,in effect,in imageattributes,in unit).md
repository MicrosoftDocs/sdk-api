---
UID: NF:gdiplusgraphics.Graphics.DrawImage(IN Image,IN RectF,IN Matrix,IN Effect,IN ImageAttributes,IN Unit)
title: Graphics::DrawImage(IN Image,IN RectF,IN Matrix,IN Effect,IN ImageAttributes,IN Unit)
author: windows-sdk-content
description: The method draws a portion of an image after applying a specified effect.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_sourceRect_Matrix_xForm_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawimagemethods\drawimage_imageimage_rectfsourcerect_matrixxform.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: DrawImage, DrawImage method [GDI+], DrawImage method [GDI+],Graphics class, Graphics class [GDI+],DrawImage method, Graphics.DrawImage, Graphics.DrawImage(IN Image,IN RectF,IN Matrix,IN Effect,IN ImageAttributes,IN Unit), Graphics.DrawImage(Image*,RectF*,Matrix*,Effect*,ImageAttributes*,Unit*), Graphics::DrawImage, Graphics::DrawImage(IN Image,IN RectF,IN Matrix,IN Effect,IN ImageAttributes,IN Unit), _gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_sourceRect_Matrix_xForm_, gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_sourceRect_Matrix_xForm_
ms.prod: windows-hardware
ms.technology: windows-devices
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

Type: <b><a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object that specifies the image to be drawn. 


### -param sourceRect [in]

Type: <b><a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a> object that specifies the portion of the image to be drawn.


### -param xForm [in]

Type: <b><a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that specifies the parallelogram in which the image portion is rendered. The destination parallelogram is calculated by applying the affine transformation stored in the matrix to the source rectangle.


### -param effect [in]

Type: <b><a href="https://msdn.microsoft.com/7b32aad2-ba44-46a6-8315-d55fed2d9391">Effect</a>*</b>

Pointer to a instance of a descendant of the <a href="https://msdn.microsoft.com/7b32aad2-ba44-46a6-8315-d55fed2d9391">Effect</a> class. The descendant specifies an effect or adjustment (for example, a change in contrast) that is applied to the image before rendering. The image is not permanently altered by the effect.


### -param imageAttributes [in]

Type: <b><a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object that specifies color adjustments to be applied when the image is rendered. Can be <b>NULL</b>.


### -param srcUnit [in]

Type: <b><a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">Unit</a>*</b>

Element of the <a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">Unit</a> enumeration that specifies the unit of measure for the source rectangle.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/0ad2a132-6db6-4099-81a2-10e1cd1b1f61">Drawing, Positioning, and Cloning Images</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/8c1a26d9-b640-4f38-8276-10c4464525f2">Loading and Displaying Bitmaps</a>
 

 

