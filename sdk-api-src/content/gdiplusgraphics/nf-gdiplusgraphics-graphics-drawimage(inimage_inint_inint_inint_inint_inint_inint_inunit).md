---
UID: NF:gdiplusgraphics.Graphics.DrawImage(IN Image,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN Unit)
title: Graphics::DrawImage(IN Image,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN Unit) (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::DrawImage method draws an image.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawImage_Image_image_INT_x_INT_y_INT_srcx_INT_srcy_INT_srcwidth_INT_srcheig.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawimagemethods\drawimage_96imageimage_intx_inty_intsrcx_intsrcy_i.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrawImage, DrawImage method [GDI+], DrawImage method [GDI+],Graphics class, Graphics class [GDI+],DrawImage method, Graphics.DrawImage, Graphics.DrawImage(IN Image,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN Unit), Graphics.DrawImage(Image*,INT,INT,INT,INT,INT,INT,Unit), Graphics::DrawImage, Graphics::DrawImage(IN Image,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN Unit), _gdiplus_CLASS_Graphics_DrawImage_Image_image_INT_x_INT_y_INT_srcx_INT_srcy_INT_srcwidth_INT_srcheig, gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_INT_x_INT_y_INT_srcx_INT_srcy_INT_srcwidth_INT_srcheig
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

# Graphics::DrawImage(IN Image,IN INT,IN INT,IN INT,IN INT,IN INT,IN INT,IN Unit)


## -description


The <b>Graphics::DrawImage</b> method draws an image.


## -parameters




### -param image [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object that specifies the source image. 


### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the upper-left corner of the destination position at which to draw the image. 


### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the upper-left corner of the destination position at which to draw the image. 


### -param srcx [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the upper-left corner of the portion of the source image to be drawn. 


### -param srcy [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the upper-left corner of the portion of the source image to be drawn. 


### -param srcwidth [in]

Type: <b>INT</b>

Integer that specifies the width of the portion of the source image to be drawn. 


### -param srcheight [in]

Type: <b>INT</b>

Integer that specifies the height of the portion of the source image to be drawn. 


### -param srcUnit [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534405(v=VS.85).aspx">Unit</a></b>

Element of the 
					<a href="https://msdn.microsoft.com/en-us/library/ms534405(v=VS.85).aspx">Unit</a> enumeration that specifies the unit of measure for the image. The default value is UnitPixel. 


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
 

 

