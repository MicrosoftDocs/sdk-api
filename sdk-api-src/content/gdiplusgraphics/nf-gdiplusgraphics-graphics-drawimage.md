---
UID: NF:gdiplusgraphics.Graphics.DrawImage
title: Graphics::DrawImage
description: The Graphics::DrawImage method draws an image.
ms.assetid: 933bdaec-75a8-4437-b42a-0799c2925d66
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: Graphics::DrawImage
ms.topic: language-reference
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdiplusgraphics.h
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
 - gdiplusgraphics.h
api_name:
 - Graphics::DrawImage
---

# DrawImage(Image*,PointF&)

## -description

The **Graphics::DrawImage** method draws an image.

## -parameters

### -param image

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object that specifies the source image.

### -param point

Reference to a <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a> object that specifies the coordinates of the upper-left corner of the destination position at which to draw the image.

## -returns

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example draws an image.
The image is drawn with the upper-left corner at the coordinate specified by the *point* parameter.

```cpp
VOID Example_DrawImage8(HDC hdc)

{

   Graphics graphics(hdc);

   // Create an Image object.
   Image image(L"climber.jpg");

   // Draw the image.
   graphics.DrawImage(&image, PointF(0.0f, 0.0f));
}
```

## -see-also

<a href="https://msdn.microsoft.com/en-us/library/ms536388(v=VS.85).aspx">Drawing, Positioning, and Cloning Images</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533830(v=VS.85).aspx">Loading and Displaying Bitmaps</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>
