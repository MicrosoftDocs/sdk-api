---
UID: NF:gdiplusgraphics.Graphics.SetClip(IN HRGN,IN CombineMode)
title: Graphics::SetClip(IN HRGN,IN CombineMode)
author: windows-sdk-content
description: The Graphics::SetClip method updates the clipping region of this Graphics object to a region that is the combination of itself and a Windows Graphics Device Interface (GDI) region.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetClip_hRgn_combineMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicssetclipmethods\setclip_93hrgn_combinemode.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Graphics class [GDI+],SetClip method, Graphics.SetClip, Graphics.SetClip(HRGN,CombineMode), Graphics.SetClip(IN HRGN,IN CombineMode), Graphics::SetClip, Graphics::SetClip(IN HRGN,IN CombineMode), SetClip, SetClip method [GDI+], SetClip method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetClip_hRgn_combineMode_, gdiplus._gdiplus_CLASS_Graphics_SetClip_hRgn_combineMode_
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
 - Graphics.SetClip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusgraphics.h
: 
- Graphics.SetClip
: 
req.product: GDI+ 1.0
---

# Graphics::SetClip(IN HRGN,IN CombineMode)


## -description


The <b>Graphics::SetClip</b> method updates the clipping region of this  <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object to a region that is the combination of itself and a Windows Graphics Device Interface (GDI) region.


## -parameters




### -param hRgn [in]

Type: <b>HRGN</b>

Handle to a GDI region to be combined with the clipping region of this <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. This is provided for legacy code. New applications should pass a <a href="https://msdn.microsoft.com/2972b879-7d2f-4cad-b17d-670125f43691">Region</a> object as the first parameter. 


### -param combineMode [in]

Type: <b><a href="https://msdn.microsoft.com/8cdb8aab-7918-421a-bc64-e8c91d1b866e">CombineMode</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/8cdb8aab-7918-421a-bc64-e8c91d1b866e">CombineMode</a> enumeration that specifies how the GDI region is combined with the clipping region of this <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. The default value is CombineModeReplace. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




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




<a href="https://msdn.microsoft.com/58cc052d-31af-4410-81b9-defbad08a1dc">Clipping</a>



<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/8cdb8aab-7918-421a-bc64-e8c91d1b866e">CombineMode</a>



<a href="https://msdn.microsoft.com/b46ce1d3-c2b5-4dbf-86b7-2e6f52ab2787">GetClipBounds Methods</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/5a1f3e79-34c6-4974-a877-3cea75ecb9cc">Graphics::GetClip</a>



<a href="https://msdn.microsoft.com/1a0503da-1d93-4eef-9c0f-dbd257dc8a5d">Graphics::IsClipEmpty</a>



<a href="https://msdn.microsoft.com/f3fcb50c-30c3-4a57-ab99-ebe7d05ede8f">Graphics::ResetClip</a>



<a href="https://msdn.microsoft.com/52c0b29a-73a8-4bf5-9e8d-950d72d8a9bf">IntersectClip Methods</a>



<a href="https://msdn.microsoft.com/2ae4af90-2612-4b00-b47d-0155e98bffa5">TranslateClip Methods</a>
 

 

