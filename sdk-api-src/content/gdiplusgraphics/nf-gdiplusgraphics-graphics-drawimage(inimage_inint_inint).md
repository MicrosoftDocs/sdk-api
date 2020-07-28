---
UID: NF:gdiplusgraphics.Graphics.DrawImage(INImage,ININT,ININT)
title: Graphics::DrawImage(IN Image,IN INT,IN INT) (gdiplusgraphics.h)
description: The Graphics::DrawImage method draws an image at a specified location.
helpviewer_keywords: ["DrawImage","DrawImage method [GDI+]","DrawImage method [GDI+]","Graphics class","Graphics class [GDI+]","DrawImage method","Graphics.DrawImage","Graphics.DrawImage(IN Image","IN INT","IN INT)","Graphics.DrawImage(Image*","INT","INT)","Graphics::DrawImage","Graphics::DrawImage(IN Image","IN INT","IN INT)","_gdiplus_CLASS_Graphics_DrawImage_Image_image_INT_x_INT_y_","gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_INT_x_INT_y_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawImage_Image_image_INT_x_INT_y_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawimagemethods\drawimage_18imageimage_intx_inty.htm
ms.date: 12/05/2018
ms.keywords: DrawImage, DrawImage method [GDI+], DrawImage method [GDI+],Graphics class, Graphics class [GDI+],DrawImage method, Graphics.DrawImage, Graphics.DrawImage(IN Image,IN INT,IN INT), Graphics.DrawImage(Image*,INT,INT), Graphics::DrawImage, Graphics::DrawImage(IN Image,IN INT,IN INT), _gdiplus_CLASS_Graphics_DrawImage_Image_image_INT_x_INT_y_, gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_INT_x_INT_y_
f1_keywords:
- gdiplusgraphics/Graphics.DrawImage
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::DrawImage(IN Image,IN INT,IN INT)


## -description


The <b>Graphics::DrawImage</b> method draws an image at a specified location.


## -parameters




### -param image [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>*</b>

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object that specifies the image to be drawn. 


### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the upper-left corner of the rendered image. 


### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the upper-left corner of the rendered image. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-drawing-positioning-and-cloning-images-about">Drawing, Positioning, and Cloning Images</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-bitmaps-use">Loading and Displaying Bitmaps</a>
 

 

