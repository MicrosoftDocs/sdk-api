---
UID: NF:gdiplusgraphics.Graphics.IsClipEmpty
title: Graphics::IsClipEmpty
author: windows-sdk-content
description: The Graphics::IsClipEmpty method determines whether the clipping region of this Graphics object is empty.
old-location: gdiplus\_gdiplus_CLASS_Graphics_IsClipEmpty_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\isclipempty.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Graphics class [GDI+],IsClipEmpty method, Graphics.IsClipEmpty, Graphics::IsClipEmpty, IsClipEmpty, IsClipEmpty method [GDI+], IsClipEmpty method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_IsClipEmpty_, gdiplus._gdiplus_CLASS_Graphics_IsClipEmpty_
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
 - Graphics.IsClipEmpty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::IsClipEmpty


## -description


The <b>Graphics::IsClipEmpty</b> method determines whether the clipping region of this <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object is empty.


## -parameters






## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the clipping region of a <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object is empty, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -remarks



If the clipping region of a <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object is empty, there is no area left in which to draw. Consequently, nothing will be drawn when the clipping region is empty.


#### Examples



The following example determines whether the clipping region is empty and, if it isn't, draws a rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_IsClipEmpty(HDC hdc)
{
   Graphics graphics(hdc);

   // If the clipping region is not empty, draw a rectangle.
   if (!graphics.IsClipEmpty())
   {
   graphics.DrawRectangle(&amp;Pen(Color(255, 0, 0, 0), 3), 0, 0, 100, 100);
   }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536360(v=VS.85).aspx">Clipping</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535780(v=VS.85).aspx">GetClipBounds Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535698(v=VS.85).aspx">Graphics::GetClip</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535794(v=VS.85).aspx">Graphics::IsVisibleClipEmpty</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535802(v=VS.85).aspx">Graphics::ResetClip</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535789(v=VS.85).aspx">SetClip Methods</a>
 

 

