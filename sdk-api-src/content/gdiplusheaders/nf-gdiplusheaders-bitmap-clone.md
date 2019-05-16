---
UID: NF:gdiplusheaders.Bitmap.Clone
title: Bitmap::Clone
description: The Bitmap::Clone method creates a new Bitmap object by copying a portion of this bitmap.
ms.assetid: 68c03673-ad3c-43b7-a21d-23192de7ad19
ms.author: windowssdkdev
ms.date: 05/20/2019
ms.keywords: Bitmap::Clone
ms.topic: language-reference
targetos: Windows
product: Windows
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

The **Bitmap::Clone** method creates a new <a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a> object by copying a portion of this bitmap.

## -parameters

### -param rect

Reference to a rectangle that specifies the portion of this bitmap to be copied.

### -param format

Integer that specifies the pixel format of the new bitmap.
The **PixelFormat** data type and constants that represent various pixel formats are defined in Gdipluspixelformats.h.
For more information about pixel format constants, see <a href="https://msdn.microsoft.com/en-us/library/ms534412(v=VS.85).aspx">Image Pixel Format Constants</a>.

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

<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536287(v=VS.85).aspx">Clone</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534412(v=VS.85).aspx">Image Pixel Format Constants</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533815(v=VS.85).aspx">Using Images, Bitmaps, and Metafiles</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536335(v=VS.85).aspx">Images, Bitmaps, and Metafiles</a>
