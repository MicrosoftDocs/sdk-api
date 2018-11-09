---
UID: NF:gdiplusgraphics.Graphics.GetClipBounds(OUT Rect)
title: Graphics::GetClipBounds(OUT Rect)
author: windows-sdk-content
description: The Graphics::GetClipBounds method gets a rectangle that encloses the clipping region of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetClipBounds_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsgetclipboundsmethods\getclipbounds.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetClipBounds, GetClipBounds method [GDI+], GetClipBounds method [GDI+],Graphics class, Graphics class [GDI+],GetClipBounds method, Graphics.GetClipBounds, Graphics.GetClipBounds(OUT Rect), Graphics.GetClipBounds(Rect*), Graphics::GetClipBounds, Graphics::GetClipBounds(OUT Rect), _gdiplus_CLASS_Graphics_GetClipBounds_Rect_rect_, gdiplus._gdiplus_CLASS_Graphics_GetClipBounds_Rect_rect_
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
 - Graphics.GetClipBounds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::GetClipBounds(OUT Rect)


## -description


The <b>Graphics::GetClipBounds</b> method gets a rectangle that encloses the clipping region of this <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object.


## -parameters




### -param rect [out]

Type: <b>Rect*</b>

Pointer to a <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a> object that receives the rectangle that encloses the clipping region. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The world transformation is applied to the clipping region and then the enclosing rectangle is calculated.

If you do not explicitly set the clipping region of a 
				<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object, its clipping region is infinite. When the clipping region is infinite, <b>Graphics::GetClipBounds</b> returns a large rectangle. The 
				<b>X</b> and 
				<b>Y</b> data members of that rectangle are large negative numbers, and the 
				<b>Width</b> and 
				<b>Height</b> data members are large positive numbers.


#### Examples



The following example sets a clipping region, gets the rectangle that encloses the clipping region, and then fills the rectangle.


```cpp
VOID Example_GetClipBounds(HDC hdc)
{
   Graphics graphics(hdc);

   Region   myRegion(Rect(25, 25, 100, 50));
   Rect     rect(40, 60, 100, 50);
   Region   gRegion;
   Rect     enclosingRect;

   SolidBrush  blueBrush(Color(100, 0, 0, 255));
   Pen         greenPen(Color(255, 0, 255, 0), 1.5f);

   // Modify the region by using a rectangle.
   myRegion.Union(rect);

   // Set the clipping region of the graphics object.
   graphics.SetClip(&myRegion);

   // Now, get the clipping region, and fill it.
   graphics.GetClip(&gRegion);
   graphics.FillRegion(&blueBrush, &gRegion);

   // Get a rectangle that encloses the clipping region, and draw the enclosing
   // rectangle.
   graphics.GetClipBounds(&enclosingRect);
   graphics.ResetClip();
   graphics.DrawRectangle(&greenPen, enclosingRect);}
```





## -see-also




<a href="https://msdn.microsoft.com/58cc052d-31af-4410-81b9-defbad08a1dc">Clipping</a>



<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/af7ed6de-00c3-46c8-b597-142bee9b02cc">GetVisibleClipBounds Methods</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/5a1f3e79-34c6-4974-a877-3cea75ecb9cc">Graphics::GetClip</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/e8348373-da79-4d33-8bea-d594985493d4">SetClip Methods</a>



<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a>
 

 

