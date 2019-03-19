---
UID: NF:gdiplusgraphics.Graphics.SetClip(IN HRGN,IN CombineMode)
title: Graphics::SetClip(IN HRGN,IN CombineMode) (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::SetClip method updates the clipping region of this Graphics object to a region that is the combination of itself and a Windows Graphics Device Interface (GDI) region.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetClip_hRgn_combineMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicssetclipmethods\setclip_93hrgn_combinemode.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Graphics class [GDI+],SetClip method, Graphics.SetClip, Graphics.SetClip(HRGN,CombineMode), Graphics.SetClip(IN HRGN,IN CombineMode), Graphics::SetClip, Graphics::SetClip(IN HRGN,IN CombineMode), SetClip, SetClip method [GDI+], SetClip method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetClip_hRgn_combineMode_, gdiplus._gdiplus_CLASS_Graphics_SetClip_hRgn_combineMode_
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
 - Graphics.SetClip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::SetClip(IN HRGN,IN CombineMode)


## -description


The <b>Graphics::SetClip</b> method updates the clipping region of this  <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object to a region that is the combination of itself and a Windows Graphics Device Interface (GDI) region.


## -parameters




### -param hRgn [in]

Type: <b>HRGN</b>

Handle to a GDI region to be combined with the clipping region of this <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object. This is provided for legacy code. New applications should pass a <a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a> object as the first parameter. 


### -param combineMode [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534092(v=VS.85).aspx">CombineMode</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534092(v=VS.85).aspx">CombineMode</a> enumeration that specifies how the GDI region is combined with the clipping region of this <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object. The default value is CombineModeReplace. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



This method assumes that the GDI region specified by 
				<i>hRgn</i> is already in device units, so it does not transform the coordinates of the GDI region.


#### Examples



The following example uses a GDI region to update the clipping region.


```cpp
VOID Example_SetClip2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Region object, and get its handle.
   Region region(Rect(0, 0, 100, 100));
   HRGN hRegion = region.GetHRGN(&graphics);

   // Set the clipping region with hRegion.
   graphics.SetClip(hRegion);

   // Fill a rectangle to demonstrate the clipping region.
   graphics.FillRectangle(&SolidBrush(Color(255, 0, 0, 0)), 0, 0, 500, 500);
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536360(v=VS.85).aspx">Clipping</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534092(v=VS.85).aspx">CombineMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535780(v=VS.85).aspx">GetClipBounds Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535698(v=VS.85).aspx">Graphics::GetClip</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535792(v=VS.85).aspx">Graphics::IsClipEmpty</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535802(v=VS.85).aspx">Graphics::ResetClip</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535783(v=VS.85).aspx">IntersectClip Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535791(v=VS.85).aspx">TranslateClip Methods</a>
 

 

