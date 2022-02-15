---
UID: NF:gdiplusgraphics.Graphics.DrawCachedBitmap
title: Graphics::DrawCachedBitmap (gdiplusgraphics.h)
description: The Graphics::DrawCachedBitmap method draws the image stored in a CachedBitmap object.
helpviewer_keywords: ["DrawCachedBitmap","DrawCachedBitmap method [GDI+]","DrawCachedBitmap method [GDI+]","Graphics class","Graphics class [GDI+]","DrawCachedBitmap method","Graphics.DrawCachedBitmap","Graphics::DrawCachedBitmap","_gdiplus_CLASS_Graphics_DrawCachedBitmap_cb_x_y_","gdiplus._gdiplus_CLASS_Graphics_DrawCachedBitmap_cb_x_y_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawCachedBitmap_cb_x_y_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\drawcachedbitmap.htm
ms.date: 12/05/2018
ms.keywords: DrawCachedBitmap, DrawCachedBitmap method [GDI+], DrawCachedBitmap method [GDI+],Graphics class, Graphics class [GDI+],DrawCachedBitmap method, Graphics.DrawCachedBitmap, Graphics::DrawCachedBitmap, _gdiplus_CLASS_Graphics_DrawCachedBitmap_cb_x_y_, gdiplus._gdiplus_CLASS_Graphics_DrawCachedBitmap_cb_x_y_
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
 - Graphics::DrawCachedBitmap
 - gdiplusgraphics/Graphics::DrawCachedBitmap
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
 - Graphics.DrawCachedBitmap
---

# Graphics::DrawCachedBitmap


## -description

The <b>Graphics::DrawCachedBitmap</b> method draws the image stored in a 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap">CachedBitmap</a> object.

## -parameters

### -param cb [in]

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap">CachedBitmap</a>*</b>

Pointer to a 
					<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap">CachedBitmap</a> object that contains the image to be drawn.

### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the upper-left corner of the image.

### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the upper-left corner of the image.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A 
				<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap">CachedBitmap</a> object stores an image in a format that is optimized for a particular display screen. You cannot draw a cached bitmap to a printer or to a metafile. 

Cached bitmaps will not work with any transformations other than translation.

When you construct a 
				<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap">CachedBitmap</a> object, you must pass the address of a 
				<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object to the constructor. If the screen associated with that 
				<b>Graphics</b> object has its bit depth changed after the cached bitmap is constructed, then the <b>Graphics::DrawCachedBitmap</b> method will fail, and you should reconstruct the cached bitmap. Alternatively, you can hook the display change notification message and reconstruct the cached bitmap at that time.


#### Examples



The following example calls <b>Graphics::DrawCachedBitmap</b> to draw the image stored in a 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap">CachedBitmap</a> object.


```cpp
VOID Example_DrawCachedBitmap(HDC hdc)
{
   Graphics graphics(hdc);

   // Create Bitmap object.
   Bitmap bitmap(L"Climber.jpg");

   // Use the Bitmap object to create a CachedBitmap object.
   CachedBitmap cachedBitmap(&bitmap, &graphics);

   // Draw the cached bitmap.
   graphics.DrawCachedBitmap(&cachedBitmap, 20, 10);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/gdiplus/-gdiplus-drawing-positioning-and-cloning-images-about">Drawing, Positioning, and Cloning Images</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-cached-bitmap-to-improve-performance-use">Using a Cached Bitmap to Improve Performance</a>