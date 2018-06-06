---
UID: NF:gdiplusgraphics.Graphics.IsClipEmpty
title: Graphics::IsClipEmpty
author: windows-sdk-content
description: The Graphics::IsClipEmpty method determines whether the clipping region of this Graphics object is empty.
old-location: gdiplus\_gdiplus_CLASS_Graphics_IsClipEmpty_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\isclipempty.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Graphics class [GDI+],IsClipEmpty method, Graphics.IsClipEmpty, Graphics::IsClipEmpty, IsClipEmpty, IsClipEmpty method [GDI+], IsClipEmpty method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_IsClipEmpty_, gdiplus._gdiplus_CLASS_Graphics_IsClipEmpty_
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
tech.root: 
req.typenames: 
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::IsClipEmpty


## -description


The <b>Graphics::IsClipEmpty</b> method determines whether the clipping region of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object is empty.


## -parameters






## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the clipping region of a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object is empty, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -remarks



If the clipping region of a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object is empty, there is no area left in which to draw. Consequently, nothing will be drawn when the clipping region is empty.


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




<a href="https://msdn.microsoft.com/58cc052d-31af-4410-81b9-defbad08a1dc">Clipping</a>



<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/b46ce1d3-c2b5-4dbf-86b7-2e6f52ab2787">GetClipBounds Methods</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/5a1f3e79-34c6-4974-a877-3cea75ecb9cc">Graphics::GetClip</a>



<a href="https://msdn.microsoft.com/73733baf-6cbf-4220-b89d-0cd6856acc46">Graphics::IsVisibleClipEmpty</a>



<a href="https://msdn.microsoft.com/f3fcb50c-30c3-4a57-ab99-ebe7d05ede8f">Graphics::ResetClip</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn915769">Region</a>



<a href="https://msdn.microsoft.com/e8348373-da79-4d33-8bea-d594985493d4">SetClip Methods</a>
 

 

