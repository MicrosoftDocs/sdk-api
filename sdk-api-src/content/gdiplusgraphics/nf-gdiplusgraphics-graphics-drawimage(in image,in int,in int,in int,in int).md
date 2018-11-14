---
UID: NF:gdiplusgraphics.Graphics.DrawImage(IN Image,IN INT,IN INT,IN INT,IN INT)
title: Graphics::DrawImage(IN Image,IN INT,IN INT,IN INT,IN INT)
author: windows-sdk-content
description: The Graphics::DrawImage method draws an image.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawImage_Image_image_INT_x_INT_y_INT_width_INT_height_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawimagemethods\drawimage_62imageimage_intx_inty_intwidth_intheigh.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DrawImage, DrawImage method [GDI+], DrawImage method [GDI+],Graphics class, Graphics class [GDI+],DrawImage method, Graphics.DrawImage, Graphics.DrawImage(IN Image,IN INT,IN INT,IN INT,IN INT), Graphics.DrawImage(Image*,INT,INT,INT,INT), Graphics::DrawImage, Graphics::DrawImage(IN Image,IN INT,IN INT,IN INT,IN INT), _gdiplus_CLASS_Graphics_DrawImage_Image_image_INT_x_INT_y_INT_width_INT_height_, gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_INT_x_INT_y_INT_width_INT_height_
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
- apiref
: 
- COM
: 
- gdiplusgraphics.h
: 
- Graphics.DrawImage
: 
req.product: GDI+ 1.0
---

# Graphics::DrawImage(IN Image,IN INT,IN INT,IN INT,IN INT)


## -description


The <b>Graphics::DrawImage</b> method draws an image.


## -parameters




### -param image [in]

Type: <b><a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object that specifies the source image. 


### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the upper-left corner of the destination rectangle at which to draw the image. 


### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the upper-left corner of the destination rectangle at which to draw the image. 


### -param width [in]

Type: <b>INT</b>

Integer that specifies the width of the destination rectangle at which to draw the image. 


### -param height [in]

Type: <b>INT</b>

Integer that specifies the height of the destination rectangle at which to draw the image. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/0ad2a132-6db6-4099-81a2-10e1cd1b1f61">Drawing, Positioning, and Cloning Images</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/8c1a26d9-b640-4f38-8276-10c4464525f2">Loading and Displaying Bitmaps</a>
 

 

