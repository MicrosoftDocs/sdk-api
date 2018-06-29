---
UID: NF:gdiplustypes.RectF.IsEmptyArea
title: RectF::IsEmptyArea
author: windows-sdk-content
description: The RectF::IsEmptyArea method determines whether this rectangle is empty.
old-location: gdiplus\_gdiplus_CLASS_RectF_IsEmptyArea_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectfclass\rectfmethods\isemptyarea_36.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IsEmptyArea, IsEmptyArea method [GDI+], IsEmptyArea method [GDI+],RectF class, RectF class [GDI+],IsEmptyArea method, RectF.IsEmptyArea, RectF::IsEmptyArea, _gdiplus_CLASS_RectF_IsEmptyArea_, gdiplus._gdiplus_CLASS_RectF_IsEmptyArea_
ms.prod: windows
ms.technology: windows-sdk
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
 - RectF.IsEmptyArea
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# RectF::IsEmptyArea


## -description


The <b>RectF::IsEmptyArea</b> method determines whether this rectangle is empty.


## -parameters






## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the rectangle is empty, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -remarks



A rectangle is defined as empty if either the width or the height is zero or less.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/library/ms534497(v=VS.85).aspx">RectF</a> object, inflates the dimensions of the rectangle, and determines whether the rectangle is empty.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_IsEmptyArea(HDC hdc)
{
   Graphics graphics(hdc);
   RectF rect(50, 50, 200, 100);
   rect.Inflate(0, -120);

   if(rect.IsEmptyArea())

   // The rectangle does not enclose any area.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/ms534944(v=VS.85).aspx">Inflate Methods</a>



<a href="https://msdn.microsoft.com/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">Rect</a>



<a href="https://msdn.microsoft.com/library/ms534497(v=VS.85).aspx">RectF</a>



<a href="https://msdn.microsoft.com/library/ms533855(v=VS.85).aspx">Using a Pen to Draw Lines and Rectangles</a>
 

 

