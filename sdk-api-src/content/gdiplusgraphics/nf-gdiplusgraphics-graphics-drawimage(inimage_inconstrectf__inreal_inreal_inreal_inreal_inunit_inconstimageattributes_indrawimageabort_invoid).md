---
UID: NF:gdiplusgraphics.Graphics.DrawImage(IN Image,IN const RectF &,IN REAL,IN REAL,IN REAL,IN REAL,IN Unit,IN const ImageAttributes,IN DrawImageAbort,IN VOID)
title: Graphics::DrawImage(IN Image,IN const RectF &,IN REAL,IN REAL,IN REAL,IN REAL,IN Unit,IN const ImageAttributes,IN DrawImageAbort,IN VOID) (gdiplusgraphics.h)
description: The Graphics::DrawImage method draws an image.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_destRect_REAL_srcx_REAL_srcy_REAL_srcwidth_REAL_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawimagemethods\drawimage_96imageimage_rectfampdestrect_realsrcx_r.htm
ms.date: 12/05/2018
ms.keywords: DrawImage, DrawImage method [GDI+], DrawImage method [GDI+],Graphics class, Graphics class [GDI+],DrawImage method, Graphics.DrawImage, Graphics.DrawImage(IN Image,IN const RectF &,IN REAL,IN REAL,IN REAL,IN REAL,IN Unit,IN const ImageAttributes,IN DrawImageAbort,IN VOID), Graphics.DrawImage(Image*,const RectF&,REAL,REAL,REAL,REAL,Unit,ImageAttributes*,DrawImageAbort,VOID*), Graphics::DrawImage, Graphics::DrawImage(IN Image,IN const RectF &,IN REAL,IN REAL,IN REAL,IN REAL,IN Unit,IN const ImageAttributes,IN DrawImageAbort,IN VOID), _gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_destRect_REAL_srcx_REAL_srcy_REAL_srcwidth_REAL_, gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_RectF_destRect_REAL_srcx_REAL_srcy_REAL_srcwidth_REAL_
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

# Graphics::DrawImage(IN Image,IN const RectF &,IN REAL,IN REAL,IN REAL,IN REAL,IN Unit,IN const ImageAttributes,IN DrawImageAbort,IN VOID)


## -description


The <b>Graphics::DrawImage</b> method draws an image.


## -parameters




### -param image [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>*</b>

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object that specifies the source image. 


### -param destRect [in, ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a></b>

Reference to a rectangle that bounds the drawing area for the image. 


### -param srcx [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the upper-left corner of the portion of the source image to be drawn. 


### -param srcy [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the upper-left corner of the portion of the source image to be drawn. 


### -param srcwidth [in]

Type: <b>REAL</b>

Real number that specifies the width of the portion of the source image to be drawn. 


### -param srcheight [in]

Type: <b>REAL</b>

Real number that specifies the height of the portion of the source image to be drawn. 


### -param srcUnit [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a></b>

Element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a> enumeration that specifies the unit of measure for the image. The default value is <b>UnitPixel</b>. 


### -param imageAttributes [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>*</b>

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object that specifies the color and size attributes of the image to be drawn. The default value is <b>NULL</b>. 


### -param callback [in]

Type: <b>DrawImageAbort</b>

Callback method used to cancel the drawing in progress. The default value is <b>NULL</b>. 


### -param callbackData [in]

Type: <b>VOID*</b>

Pointer to additional data used by the method specified by the 
					<i>callback</i> parameter. The default value is <b>NULL</b>. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -remarks



The portion of the source image to be drawn is scaled to fit the rectangle.


#### Examples



The following example draws the original source image and then draws a portion of the image in a specified rectangle.


```cpp
VOID Example_DrawImage6(HDC hdc)

{

   Graphics graphics(hdc);



   // Create an Image object.

   Image image(L"pattern.png");



   // Draw the original source image.

   graphics.DrawImage(&image, 10, 10);



   // Define the portion of the image to draw.

   REAL srcX = 70.0f;

   REAL srcY = 20.0f;

   REAL srcWidth = 100.0f;

   REAL srcHeight = 100.0f;



   // Create a RectF object that specifies the destination of the image.

   RectF destRect(200.0f, 10.0f, <REAL>image.GetWidth(), <REAL>image.GetHeight());

   

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

<img alt="Illustration showing two graphics: a multicolored checkerboard pattern, then a two-toned enlargement from that pattern" src="images/drawimage3.png"/>

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-drawing-positioning-and-cloning-images-about">Drawing, Positioning, and Cloning Images</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-bitmaps-use">Loading and Displaying Bitmaps</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable">SetRemapTable</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a>
 

 

