---
UID: NF:gdiplustypes.Rect.IsEmptyArea
title: Rect::IsEmptyArea
author: windows-sdk-content
description: The Rect::IsEmptyArea method determines whether this rectangle is empty.
old-location: gdiplus\_gdiplus_CLASS_Rect_IsEmptyArea_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectclass\rectmethods\isemptyarea.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IsEmptyArea, IsEmptyArea method [GDI+], IsEmptyArea method [GDI+],Rect class, Rect class [GDI+],IsEmptyArea method, Rect.IsEmptyArea, Rect::IsEmptyArea, _gdiplus_CLASS_Rect_IsEmptyArea_, gdiplus._gdiplus_CLASS_Rect_IsEmptyArea_
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
 - Rect.IsEmptyArea
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
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
						<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">Rect</a> object, inflates the dimensions of the rectangle, and determines whether the rectangle is empty.

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




<a href="https://msdn.microsoft.com/4875dec3-e57e-4109-8c63-c3dc4db6080d">Inflate Methods</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">Rect</a>



<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a>



<a href="https://msdn.microsoft.com/f2e4144f-f2f1-49db-bfdf-ffce3023b4cb">Using a Pen to Draw Lines and Rectangles</a>
 

 

