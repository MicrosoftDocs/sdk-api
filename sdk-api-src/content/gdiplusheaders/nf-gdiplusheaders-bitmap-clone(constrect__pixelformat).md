---
UID: NF:gdiplusheaders.Bitmap.Clone(constRect&,PixelFormat)
title: Bitmap::Clone
description: The Bitmap::Clone method creates a new Bitmap object by copying a portion of this bitmap. (overload 1/2)
tech.root: gdiplus
helpviewer_keywords: ["Bitmap::Clone"]
ms.assetid: 68c03673-ad3c-43b7-a21d-23192de7ad19
ms.date: 05/20/2019
ms.keywords: Bitmap::Clone
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdiplusheaders.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - Bitmap::Clone
 - gdiplusheaders/Bitmap::Clone
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - Bitmap::Clone
---

# Bitmap::Clone(Rect&,PixelFormat)


## -description

The **Bitmap::Clone** method creates a new <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object by copying a portion of this bitmap.

## -parameters

### -param rect

Reference to a rectangle that specifies the portion of this bitmap to be copied.

### -param format

Integer that specifies the pixel format of the new bitmap.
The **PixelFormat** data type and constants that represent various pixel formats are defined in Gdipluspixelformats.h.
For more information about pixel format constants, see <a href="/windows/desktop/gdiplus/-gdiplus-constant-image-pixel-format-constants">Image Pixel Format Constants</a>.

## -returns

Type: Bitmap*

This method returns a pointer to the new Bitmap object.

## -remarks

#### Examples

The following example creates a Bitmap object from an image file, clones the upper-left portion of the image, and then draws the cloned image.

```cpp
VOID Example_Clone(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Bitmap object from a JPEG file.
   Bitmap bitmap(L"Climber.jpg");

   // Clone a portion of the bitmap.
   Bitmap* clone = bitmap.Clone(Rect(0, 0, 100, 100), PixelFormatDontCare);

   // Draw the clone.
   graphics.DrawImage(clone, 0, 0);

   delete clone;
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>

<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)">Clone</a>

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>

<a href="/windows/desktop/gdiplus/-gdiplus-constant-image-pixel-format-constants">Image Pixel Format Constants</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>

<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>

<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>
