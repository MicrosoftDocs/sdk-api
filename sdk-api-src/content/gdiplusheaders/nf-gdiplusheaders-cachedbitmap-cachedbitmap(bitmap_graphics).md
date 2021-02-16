---
UID: NF:gdiplusheaders.CachedBitmap.CachedBitmap(Bitmap,Graphics)
title: CachedBitmap::CachedBitmap(IN Bitmap,IN Graphics) (gdiplusheaders.h)
description: Creates a CachedBitmap::CachedBitmap object based on a Bitmap object and a Graphics object.
helpviewer_keywords: ["CachedBitmap","CachedBitmap class [GDI+]","CachedBitmap constructor","CachedBitmap constructor [GDI+]","CachedBitmap constructor [GDI+]","CachedBitmap class","CachedBitmap.CachedBitmap","CachedBitmap.CachedBitmap(IN Bitmap","IN Graphics)","CachedBitmap::CachedBitmap","CachedBitmap::CachedBitmap(IN Bitmap","IN Graphics)","_gdiplus_CLASS_CachedBitmap_CachedBitmap_bitmap_graphics_","gdiplus._gdiplus_CLASS_CachedBitmap_CachedBitmap_bitmap_graphics_"]
old-location: gdiplus\_gdiplus_CLASS_CachedBitmap_CachedBitmap_bitmap_graphics_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\cachedbitmapclass\cachedbitmap_55bitmap_graphics.htm
ms.date: 12/05/2018
ms.keywords: CachedBitmap, CachedBitmap class [GDI+],CachedBitmap constructor, CachedBitmap constructor [GDI+], CachedBitmap constructor [GDI+],CachedBitmap class, CachedBitmap.CachedBitmap, CachedBitmap.CachedBitmap(IN Bitmap,IN Graphics), CachedBitmap::CachedBitmap, CachedBitmap::CachedBitmap(IN Bitmap,IN Graphics), _gdiplus_CLASS_CachedBitmap_CachedBitmap_bitmap_graphics_, gdiplus._gdiplus_CLASS_CachedBitmap_CachedBitmap_bitmap_graphics_
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
 - CachedBitmap::CachedBitmap
 - gdiplusheaders/CachedBitmap::CachedBitmap
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
 - CachedBitmap.CachedBitmap
---

## -description

Creates a <b>CachedBitmap::CachedBitmap</b> object based on a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object and a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. The cached bitmap takes the pixel data from the <b>Bitmap</b> object and stores it in a format that is optimized for the display device associated with the <b>Graphics</b> object.

## -parameters

### -param bitmap

Type: [in] <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object that contains the pixel data to be optimized.

### -param graphics

Type: [in] <b><a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that is associated with a display device for which the image will be optimized.

## -remarks

You can display a cached bitmap by passing the address of a <b>CachedBitmap::CachedBitmap</b> object to the 
				<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap">DrawCachedBitmap</a> method of a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. Use the <b>Graphics</b> object that was passed to the <b>CachedBitmap::CachedBitmap</b> constructor or another <b>Graphics</b> object that represents the same device.


## Examples



The following example creates a <b>CachedBitmap::CachedBitmap</b> object based on a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object and a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. The code calls the 
						<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap">DrawCachedBitmap</a> method of that <b>Graphics</b> object to display the cached bitmap.

```cpp
VOID Example_CachedBitmap(HDC hdc)
{
   Graphics graphics(hdc);
   Bitmap bitmap(L"Grapes.jpg");
   CachedBitmap cachedBitmap(&bitmap, &graphics);

   graphics.DrawCachedBitmap(&cachedBitmap, 10, 10);  
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap">CachedBitmap</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-cached-bitmap-to-improve-performance-use">Using a Cached Bitmap to Improve Performance</a>