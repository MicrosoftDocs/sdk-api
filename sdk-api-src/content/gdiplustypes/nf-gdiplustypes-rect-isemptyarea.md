---
UID: NF:gdiplustypes.Rect.IsEmptyArea
title: Rect::IsEmptyArea
author: windows-sdk-content
description: The Rect::IsEmptyArea method determines whether this rectangle is empty.
old-location: gdiplus\_gdiplus_CLASS_Rect_IsEmptyArea_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectclass\rectmethods\isemptyarea.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IsEmptyArea, IsEmptyArea method [GDI+], IsEmptyArea method [GDI+],Rect class, Rect class [GDI+],IsEmptyArea method, Rect.IsEmptyArea, Rect::IsEmptyArea, _gdiplus_CLASS_Rect_IsEmptyArea_, gdiplus._gdiplus_CLASS_Rect_IsEmptyArea_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplustypes.h
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
 - Rect.IsEmptyArea
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplustypes.h
: 
- Rect.IsEmptyArea
: 
req.product: GDI+ 1.0
---

# Rect::IsEmptyArea


## -description


The <b>Rect::IsEmptyArea</b> method determines whether this rectangle is empty.


## -parameters






## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the rectangle is empty, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -remarks



A rectangle is defined as empty if either the width or the height is zero or less.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a> object, inflates the dimensions of the rectangle, and determines whether the rectangle is empty.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_IsEmptyArea(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Rect object, and inflate the dimensions.
   Rect rect(50, 50, 200, 100);
   rect.Inflate(0, -120);

   // Determine whether the rectangle is empty.
   if(rect.IsEmptyArea())

   // The rectangle does not enclose any area.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534974(v=VS.85).aspx">Inflate Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533855(v=VS.85).aspx">Using a Pen to Draw Lines and Rectangles</a>
 

 

