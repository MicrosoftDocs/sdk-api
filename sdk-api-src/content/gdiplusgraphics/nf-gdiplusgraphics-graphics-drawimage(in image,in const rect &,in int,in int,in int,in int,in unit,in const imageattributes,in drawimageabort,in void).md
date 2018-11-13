---
UID: NF:gdiplusgraphics.Graphics.DrawImage(IN Image,IN const Rect &,IN INT,IN INT,IN INT,IN INT,IN Unit,IN const ImageAttributes,IN DrawImageAbort,IN VOID)
title: Graphics::DrawImage(IN Image,IN const Rect &,IN INT,IN INT,IN INT,IN INT,IN Unit,IN const ImageAttributes,IN DrawImageAbort,IN VOID)
author: windows-sdk-content
description: The Graphics::DrawImage method draws an image.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawImage_Image_image_Rect_destRect_INT_srcx_INT_srcy_INT_srcwidth_INT_srche.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawimagemethods\drawimage_72imageimage_rectampdestrect_intsrcx_int.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DrawImage, DrawImage method [GDI+], DrawImage method [GDI+],Graphics class, Graphics class [GDI+],DrawImage method, Graphics.DrawImage, Graphics.DrawImage(IN Image,IN const Rect &,IN INT,IN INT,IN INT,IN INT,IN Unit,IN const ImageAttributes,IN DrawImageAbort,IN VOID), Graphics.DrawImage(Image*,const Rect&,INT,INT,INT,INT,Unit,ImageAttributes*,DrawImageAbort,VOID*), Graphics::DrawImage, Graphics::DrawImage(IN Image,IN const Rect &,IN INT,IN INT,IN INT,IN INT,IN Unit,IN const ImageAttributes,IN DrawImageAbort,IN VOID), _gdiplus_CLASS_Graphics_DrawImage_Image_image_Rect_destRect_INT_srcx_INT_srcy_INT_srcwidth_INT_srche, gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_Rect_destRect_INT_srcx_INT_srcy_INT_srcwidth_INT_srche
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

# Graphics::DrawImage(IN Image,IN const Rect &,IN INT,IN INT,IN INT,IN INT,IN Unit,IN const ImageAttributes,IN DrawImageAbort,IN VOID)


## -description


The <b>Graphics::DrawImage</b> method draws an image.


## -parameters




### -param image [in]

Type: <b><a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object that specifies the source image. 


### -param destRect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a></b>

Reference to a rectangle that bounds the drawing area for the image. 


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

Type: <b><a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">Unit</a></b>

Element of the <a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">Unit</a> enumeration that specifies the unit of measure for the image. The default value is <b>UnitPixel</b>. 


### -param imageAttributes [in]

Type: <b><a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object that specifies the color and size attributes of the image to be drawn. The default value is <b>NULL</b>. 


### -param callback [in]

Type: <b>DrawImageAbort</b>

Callback method used to cancel the drawing in progress. The default value is <b>NULL</b>. 


### -param callbackData [in]

Type: <b>VOID*</b>

Pointer to additional data used by the method specified by the 
					<i>callback</i> parameter. The default value is <b>NULL</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The portion of the source image to be drawn is scaled to fit the rectangle.


#### Examples



The following example draws the original source image and then draws a portion of the image in a specified rectangle.


```cpp
VOID Example_DrawImage5(HDC hdc)

{
   Graphics graphics(hdc);

   // Create an Image object.
   Image image(L"pattern.png");

   // Draw the original source image.
   graphics.DrawImage(&image, 10, 10);

   // Define the portion of the image to draw.
   int srcX = 70;
   int srcY = 20;
   int srcWidth = 100;
   int srcHeight = 100;

   // Create a Rect object that specifies the destination of the image.
   Rect destRect(200, 10, image.GetWidth(), image.GetHeight());

   // Create an ImageAttributes object that specifies a recoloring from red to blue.
   ImageAttributes remapAttributes;
   ColorMap redToBlue;
   redToBlue.oldColor = Color(255, 255, 0, 0);
   redToBlue.newColor = Color(255, 0, 0, 255);
   remapAttributes.SetRemapTable(1, &redToBlue);

   // Draw the resized image.
   graphics.DrawImage(
   &image,
   destRect,
   srcX,
   srcY,
   srcWidth,
   srcHeight,
   UnitPixel,
   &remapAttributes,
   NULL,
   NULL);
}
```


The following illustration shows the output of the preceding code.

<img alt="Illustration showing two graphics: a multicolored checkerboard pattern, then a two-toned enlargement from that pattern" src="./images/drawimage3.png"/>

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0ad2a132-6db6-4099-81a2-10e1cd1b1f61">Drawing, Positioning, and Cloning Images</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>



<a href="https://msdn.microsoft.com/8c1a26d9-b640-4f38-8276-10c4464525f2">Loading and Displaying Bitmaps</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>



<a href="https://msdn.microsoft.com/87b63b0d-9071-4c7f-9ff6-14083092246a">SetRemapTable</a>



<a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">Unit</a>
 

 

