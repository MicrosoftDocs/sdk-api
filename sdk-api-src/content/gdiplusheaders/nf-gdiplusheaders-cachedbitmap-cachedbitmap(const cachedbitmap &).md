---
UID: NF:gdiplusheaders.CachedBitmap.CachedBitmap(const CachedBitmap &)
title: CachedBitmap::CachedBitmap(const CachedBitmap &)
author: windows-sdk-content
description: Creates a CachedBitmap::CachedBitmap object based on a Bitmap object and a Graphics object.
old-location: gdiplus\_gdiplus_CLASS_CachedBitmap_CachedBitmap_bitmap_graphics_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\cachedbitmapclass\cachedbitmap_55bitmap_graphics.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CachedBitmap, CachedBitmap class [GDI+],CachedBitmap constructor, CachedBitmap constructor [GDI+], CachedBitmap constructor [GDI+],CachedBitmap class, CachedBitmap.CachedBitmap, CachedBitmap.CachedBitmap(const CachedBitmap &), CachedBitmap::CachedBitmap, CachedBitmap::CachedBitmap(const CachedBitmap &), _gdiplus_CLASS_CachedBitmap_CachedBitmap_bitmap_graphics_, gdiplus._gdiplus_CLASS_CachedBitmap_CachedBitmap_bitmap_graphics_
ms.prod: windows-hardware
ms.technology: windows-devices
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

# CachedBitmap::CachedBitmap(const CachedBitmap &)


## -description


Creates a <b>CachedBitmap::CachedBitmap</b> object based on a <a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a> object and a <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. The cached bitmap takes the pixel data from the <b>Bitmap</b> object and stores it in a format that is optimized for the display device associated with the <b>Graphics</b> object.


## -parameters






#### - bitmap [in]

Type: <b><a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a> object that contains the pixel data to be optimized. 


#### - graphics [in]

Type: <b><a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object that is associated with a display device for which the image will be optimized. 


## -remarks



You can display a cached bitmap by passing the address of a <b>CachedBitmap::CachedBitmap</b> object to the 
				<a href="https://msdn.microsoft.com/9b7a2015-7d10-4b7a-88f4-c3b4d92c888d">DrawCachedBitmap</a> method of a <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. Use the <b>Graphics</b> object that was passed to the <b>CachedBitmap::CachedBitmap</b> constructor or another <b>Graphics</b> object that represents the same device.


#### Examples



The following example creates a <b>CachedBitmap::CachedBitmap</b> object based on a <a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a> object and a <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. The code calls the 
						<a href="https://msdn.microsoft.com/9b7a2015-7d10-4b7a-88f4-c3b4d92c888d">DrawCachedBitmap</a> method of that <b>Graphics</b> object to display the cached bitmap.


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




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/298880a5-cc6a-4b1a-9459-7cf6c2252328">CachedBitmap</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/42e2b664-197c-4c54-9220-b6231d6439d0">Using a Cached Bitmap to Improve Performance</a>
 

 

