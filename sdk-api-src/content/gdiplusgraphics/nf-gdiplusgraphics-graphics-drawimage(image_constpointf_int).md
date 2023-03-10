---
UID: NF:gdiplusgraphics.Graphics.DrawImage(Image,constPointF,INT)
title: Graphics::DrawImage(IN Image,IN const PointF,IN INT) (gdiplusgraphics.h)
description: The Graphics::DrawImage method draws an image. (overload 5/14)
helpviewer_keywords: ["DrawImage","DrawImage method [GDI+]","DrawImage method [GDI+]","Graphics class","Graphics class [GDI+]","DrawImage method","Graphics.DrawImage","Graphics.DrawImage(IN Image","IN const PointF","IN INT)","Graphics.DrawImage(Image*","const PointF*","INT)","Graphics::DrawImage","Graphics::DrawImage(IN Image","IN const PointF","IN INT)","_gdiplus_CLASS_Graphics_DrawImage_Image_image_PointF_destPoints_INT_count_","gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_PointF_destPoints_INT_count_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawImage_Image_image_PointF_destPoints_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawimagemethods\drawimage_44imageimage_pointfdestpoints_intcount.htm
ms.date: 12/05/2018
ms.keywords: DrawImage, DrawImage method [GDI+], DrawImage method [GDI+],Graphics class, Graphics class [GDI+],DrawImage method, Graphics.DrawImage, Graphics.DrawImage(IN Image,IN const PointF,IN INT), Graphics.DrawImage(Image*,const PointF*,INT), Graphics::DrawImage, Graphics::DrawImage(IN Image,IN const PointF,IN INT), _gdiplus_CLASS_Graphics_DrawImage_Image_image_PointF_destPoints_INT_count_, gdiplus._gdiplus_CLASS_Graphics_DrawImage_Image_image_PointF_destPoints_INT_count_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Graphics::DrawImage
 - gdiplusgraphics/Graphics::DrawImage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Graphics.DrawImage
---

# Graphics::DrawImage(IN Image,IN const PointF,IN INT)


## -description

The <b>Graphics::DrawImage</b> method draws an image.

## -parameters

### -param image [in]

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>*</b>

Pointer to an <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object that specifies the source image.

### -param destPoints [in]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>*</b>

Pointer to an array of 
					<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> objects that specify the area, in a parallelogram, in which to draw the image.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>destPoints</i> array.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The value of the 
				<i>count</i> parameter must equal 3 to specify the coordinates of the upper-left corner, upper-right corner, and lower-left corner of the parallelogram. The coordinate of the lower-right corner is calculated using the three given coordinates, the width, and the height of the image. The image is scaled to fit the parallelogram.


#### Examples



The following example draws an image.


```cpp
VOID Example_DrawImage3(HDC hdc)

{
   Graphics graphics(hdc);

   // Create an Image object.
   Image image(L"climber.jpg");

   // Create an array of PointF objects that specify the destination of the image.
   PointF destPoints[3] = {
   PointF(30.0f, 30.0f),
   PointF(250.0f, 50.0f),
   PointF(175.0f, 120.0f)};

   PointF* pdestPoints = destPoints;

   // Draw the image.
   graphics.DrawImage(&image, pdestPoints, 3);
}
```


The following illustration shows the output of the preceding code.

<img alt="Illustration showing a previously-rectangular image that has been sheared to a parallelogram" src="images/drawimage1.png"/>

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-drawing-positioning-and-cloning-images-about">Drawing, Positioning, and Cloning Images</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-bitmaps-use">Loading and Displaying Bitmaps</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>
