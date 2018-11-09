---
UID: NF:gdiplusgraphics.Graphics.ResetClip
title: Graphics::ResetClip
author: windows-sdk-content
description: The Graphics::ResetClip method sets the clipping region of this Graphics object to an infinite region.
old-location: gdiplus\_gdiplus_CLASS_Graphics_ResetClip_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\resetclip.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: Graphics class [GDI+],ResetClip method, Graphics.ResetClip, Graphics::ResetClip, ResetClip, ResetClip method [GDI+], ResetClip method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_ResetClip_, gdiplus._gdiplus_CLASS_Graphics_ResetClip_
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
 - Graphics.ResetClip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::ResetClip


## -description


The <b>Graphics::ResetClip</b> method sets the clipping region of this <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object to an infinite region.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



If the clipping region of a <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object is infinite, then items drawn by that <b>Graphics</b> object will not be clipped.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object and sets its clipping region to a rectangle. The code fills two ellipses that intersect the rectangular clipping region. The first ellipse is clipped, but the second ellipse is not clipped because it is filled after a call to <b>Graphics::ResetClip</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_ResetClip(HDC hdc)
{
   Graphics graphics(hdc);

   // Set the clipping region, and draw its outline.
   graphics.SetClip(Rect(100, 50, 200, 120));
   Pen blackPen(Color(255, 0, 0, 0), 2.0f);
   graphics.DrawRectangle(&amp;blackPen, 100, 50, 200, 120);

   // Fill a clipped ellipse in red.
   SolidBrush redBrush(Color(255, 255, 0, 0));
   graphics.FillEllipse(&amp;redBrush, 80, 40, 100, 70);

   // Reset the clipping region.
   graphics.ResetClip();

   // Fill an unclipped ellipse with blue.
   SolidBrush blueBrush(Color(255, 0, 0, 255));
   graphics.FillEllipse(&amp;blueBrush, 160, 150, 100, 60);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536360(v=VS.85).aspx">Clipping</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535698(v=VS.85).aspx">Graphics::GetClip</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535792(v=VS.85).aspx">Graphics::IsClipEmpty</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535783(v=VS.85).aspx">IntersectClip Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534770(v=VS.85).aspx">IsEmpty</a>
 

 

