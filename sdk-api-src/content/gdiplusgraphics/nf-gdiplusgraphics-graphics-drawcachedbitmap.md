---
UID: NF:gdiplusgraphics.Graphics.DrawCachedBitmap
title: Graphics::DrawCachedBitmap
author: windows-sdk-content
description: The Graphics::DrawCachedBitmap method draws the image stored in a CachedBitmap object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawCachedBitmap_cb_x_y_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\drawcachedbitmap.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: DrawCachedBitmap, DrawCachedBitmap method [GDI+], DrawCachedBitmap method [GDI+],Graphics class, Graphics class [GDI+],DrawCachedBitmap method, Graphics.DrawCachedBitmap, Graphics::DrawCachedBitmap, _gdiplus_CLASS_Graphics_DrawCachedBitmap_cb_x_y_, gdiplus._gdiplus_CLASS_Graphics_DrawCachedBitmap_cb_x_y_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - Graphics.DrawCachedBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::DrawCachedBitmap


## -description


The <b>Graphics::DrawCachedBitmap</b> method draws the image stored in a 
			<a href="https://msdn.microsoft.com/298880a5-cc6a-4b1a-9459-7cf6c2252328">CachedBitmap</a> object.


## -parameters




### -param cb [in]

Type: <b><a href="https://msdn.microsoft.com/298880a5-cc6a-4b1a-9459-7cf6c2252328">CachedBitmap</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/298880a5-cc6a-4b1a-9459-7cf6c2252328">CachedBitmap</a> object that contains the image to be drawn. 


### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the upper-left corner of the image. 


### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the upper-left corner of the image. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A 
				<a href="https://msdn.microsoft.com/298880a5-cc6a-4b1a-9459-7cf6c2252328">CachedBitmap</a> object stores an image in a format that is optimized for a particular display screen. You cannot draw a cached bitmap to a printer or to a metafile. 

Cached bitmaps will not work with any transformations other than translation.

When you construct a 
				<a href="https://msdn.microsoft.com/298880a5-cc6a-4b1a-9459-7cf6c2252328">CachedBitmap</a> object, you must pass the address of a 
				<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>object to the constructor. If the screen associated with that 
				<b>Graphics</b>object has its bit depth changed after the cached bitmap is constructed, then the <b>Graphics::DrawCachedBitmap</b> method will fail, and you should reconstruct the cached bitmap. Alternatively, you can hook the display change notification message and reconstruct the cached bitmap at that time.


#### Examples



The following example calls <b>Graphics::DrawCachedBitmap</b> to draw the image stored in a 
						<a href="https://msdn.microsoft.com/298880a5-cc6a-4b1a-9459-7cf6c2252328">CachedBitmap</a> object.


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




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/0ad2a132-6db6-4099-81a2-10e1cd1b1f61">Drawing, Positioning, and Cloning Images</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/42e2b664-197c-4c54-9220-b6231d6439d0">Using a Cached Bitmap to Improve Performance</a>
 

 

