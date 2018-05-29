---
UID: NF:gdiplusgraphics.Graphics.ResetClip
title: Graphics::ResetClip
author: windows-sdk-content
description: The Graphics::ResetClip method sets the clipping region of this Graphics object to an infinite region.
old-location: gdiplus\_gdiplus_CLASS_Graphics_ResetClip_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\resetclip.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Graphics class [GDI+],ResetClip method, Graphics.ResetClip, Graphics::ResetClip, ResetClip, ResetClip method [GDI+], ResetClip method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_ResetClip_, gdiplus._gdiplus_CLASS_Graphics_ResetClip_
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Graphics.ResetClip
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::ResetClip


## -description


The <b>Graphics::ResetClip</b> method sets the clipping region of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object to an infinite region.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



If the clipping region of a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object is infinite, then items drawn by that <b>Graphics</b> object will not be clipped.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object and sets its clipping region to a rectangle. The code fills two ellipses that intersect the rectangular clipping region. The first ellipse is clipped, but the second ellipse is not clipped because it is filled after a call to <b>Graphics::ResetClip</b>.

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




<a href="https://msdn.microsoft.com/58cc052d-31af-4410-81b9-defbad08a1dc">Clipping</a>



<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/5a1f3e79-34c6-4974-a877-3cea75ecb9cc">Graphics::GetClip</a>



<a href="https://msdn.microsoft.com/1a0503da-1d93-4eef-9c0f-dbd257dc8a5d">Graphics::IsClipEmpty</a>



<a href="https://msdn.microsoft.com/52c0b29a-73a8-4bf5-9e8d-950d72d8a9bf">IntersectClip Methods</a>



<a href="https://msdn.microsoft.com/72366100-1aec-464e-8d87-0dc88413d7cb">IsEmpty</a>
 

 

