---
UID: NF:gdiplusheaders.Image.GetBounds
title: Image::GetBounds (gdiplusheaders.h)
description: The Image::GetBounds method gets the bounding rectangle for this image.
helpviewer_keywords: ["GetBounds","GetBounds method [GDI+]","GetBounds method [GDI+]","Image class","Image class [GDI+]","GetBounds method","Image.GetBounds","Image::GetBounds","_gdiplus_CLASS_Image_GetBounds_srcRect_srcUnit_","gdiplus._gdiplus_CLASS_Image_GetBounds_srcRect_srcUnit_"]
old-location: gdiplus\_gdiplus_CLASS_Image_GetBounds_srcRect_srcUnit_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getbounds_74srcrect_srcunit.htm
ms.date: 12/05/2018
ms.keywords: GetBounds, GetBounds method [GDI+], GetBounds method [GDI+],Image class, Image class [GDI+],GetBounds method, Image.GetBounds, Image::GetBounds, _gdiplus_CLASS_Image_GetBounds_srcRect_srcUnit_, gdiplus._gdiplus_CLASS_Image_GetBounds_srcRect_srcUnit_
req.header: gdiplusheaders.h
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
 - Image::GetBounds
 - gdiplusheaders/Image::GetBounds
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
 - Image.GetBounds
---

# Image::GetBounds


## -description

The <b>Image::GetBounds</b> method gets the bounding rectangle for this image.

## -parameters

### -param srcRect [out]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a> object that receives the bounding rectangle.

### -param srcUnit [out]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a>*</b>

Pointer to a variable that receives an element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a> enumeration that indicates the unit of measure for the bounding rectangle.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The bounding rectangle for a metafile does not necessarily have (0, 0) as its upper-left corner. The coordinates of the upper-left corner can be negative or positive, depending on the drawing commands that were issued during the recording of the metafile. For example, suppose a metafile consists of a single ellipse that was recorded with the following statement:

<code>DrawEllipse(&amp;pen, 200, 100, 80, 40);</code>

Then the bounding rectangle for the metafile will enclose that one ellipse. The upper-left corner of the bounding rectangle will not be (0, 0); rather, it will be a point near (200, 100).


#### Examples

The following example creates an 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object based on a metafile and then draws the image. Next, the code calls the <b>Image::GetBounds</b> method to get the bounding rectangle for the image. The code makes two attempts to display 75 percent of the image. The first attempt fails because it specifies (0, 0) for the upper-left corner of the source rectangle. The second attempt succeeds because it uses the 
						<b>X</b> and 
						<b>Y</b> data members returned by <b>Image::GetBounds</b> to specify the upper-left corner of the source rectangle.


```cpp
VOID Example_GetBounds(HDC hdc)
{
   Graphics graphics(hdc);

   Image image(L"SampleMetafile2.emf");
   graphics.DrawImage(&image, 0, 0);

   // Get the bounding rectangle for the image (metafile).
   RectF boundsRect;
   Unit unit;
   image.GetBounds(&boundsRect, &unit);

   // Attempt to draw 75 percent of the image.
   // Less than 75 percent of the image will be visible because the
   // upper-left corner of the image's bounding rectangle is not (0, 0).
   RectF dstRect(250.0f, 0.0f, 100.0f, 50.0f);
   graphics.DrawImage(
      &image,
      dstRect,                  // destination rectangle
      0.0f, 0.0f,               // upper-left corner of source rectangle 
      0.75f*boundsRect.Width,   // width of source rectangle
      boundsRect.Height,        // height of source rectangle
      UnitPixel);

   // Draw 75 percent of the image.
   dstRect.Y = 80.0f;
   graphics.DrawImage(
      &image,
      dstRect,                       // destination rectangle
      boundsRect.X, boundsRect.Y,    // upper-left corner of source rectangle
      0.75f*boundsRect.Width,        // width of source rectangle
      boundsRect.Height,             // height of source rectangle
      UnitPixel);
}
```


The preceding code, along with a particular file, SampleMetafile2.emf, produced the following output. Note that the first attempt (upper-right) to draw 75 percent of the image shows only about 30 percent of the image.


<img alt="Screen shot showing parts of three an ellipses: all of the first one, 30% of the second, and 75% of the third " src="./images/imagegetbounds1.png"/>
<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getheight">Image::GetHeight</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getwidth">Image::GetWidth</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>