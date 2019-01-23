---
UID: NF:gdiplusheaders.CachedBitmap.CachedBitmap(IN Bitmap,IN Graphics)
title: CachedBitmap::CachedBitmap(IN Bitmap,IN Graphics)
author: windows-sdk-content
description: Creates a CachedBitmap::CachedBitmap object based on a Bitmap object and a Graphics object.
old-location: gdiplus\_gdiplus_CLASS_CachedBitmap_CachedBitmap_bitmap_graphics_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\cachedbitmapclass\cachedbitmap_55bitmap_graphics.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CachedBitmap, CachedBitmap class [GDI+],CachedBitmap constructor, CachedBitmap constructor [GDI+], CachedBitmap constructor [GDI+],CachedBitmap class, CachedBitmap.CachedBitmap, CachedBitmap.CachedBitmap(IN Bitmap,IN Graphics), CachedBitmap::CachedBitmap, CachedBitmap::CachedBitmap(IN Bitmap,IN Graphics), _gdiplus_CLASS_CachedBitmap_CachedBitmap_bitmap_graphics_, gdiplus._gdiplus_CLASS_CachedBitmap_CachedBitmap_bitmap_graphics_
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - CachedBitmap.CachedBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# CachedBitmap::CachedBitmap(IN Bitmap,IN Graphics)


## -description


Creates a <b>CachedBitmap::CachedBitmap</b> object based on a <a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a> object and a <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object. The cached bitmap takes the pixel data from the <b>Bitmap</b> object and stores it in a format that is optimized for the display device associated with the <b>Graphics</b> object.


## -parameters




#### - bitmap [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a> object that contains the pixel data to be optimized. 


#### - graphics [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object that is associated with a display device for which the image will be optimized. 


## -remarks



You can display a cached bitmap by passing the address of a <b>CachedBitmap::CachedBitmap</b> object to the 
				<a href="https://msdn.microsoft.com/en-us/library/ms535681(v=VS.85).aspx">DrawCachedBitmap</a> method of a <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object. Use the <b>Graphics</b> object that was passed to the <b>CachedBitmap::CachedBitmap</b> constructor or another <b>Graphics</b> object that represents the same device.


#### Examples



The following example creates a <b>CachedBitmap::CachedBitmap</b> object based on a <a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a> object and a <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object. The code calls the 
						<a href="https://msdn.microsoft.com/en-us/library/ms535681(v=VS.85).aspx">DrawCachedBitmap</a> method of that <b>Graphics</b> object to display the cached bitmap.


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




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534425(v=VS.85).aspx">CachedBitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533835(v=VS.85).aspx">Using a Cached Bitmap to Improve Performance</a>
 

 

