---
UID: NF:gdiplustypes.RectF.IsEmptyArea
title: RectF::IsEmptyArea
author: windows-sdk-content
description: The RectF::IsEmptyArea method determines whether this rectangle is empty.
old-location: gdiplus\_gdiplus_CLASS_RectF_IsEmptyArea_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectfclass\rectfmethods\isemptyarea_36.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: IsEmptyArea, IsEmptyArea method [GDI+], IsEmptyArea method [GDI+],RectF class, RectF class [GDI+],IsEmptyArea method, RectF.IsEmptyArea, RectF::IsEmptyArea, _gdiplus_CLASS_RectF_IsEmptyArea_, gdiplus._gdiplus_CLASS_RectF_IsEmptyArea_
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
 - RectF.IsEmptyArea
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
						<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a> object, inflates the dimensions of the rectangle, and determines whether the rectangle is empty.

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




<a href="https://msdn.microsoft.com/5f393247-0209-41b4-a97c-89e4d5d7d55d">Inflate Methods</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a>



<a href="https://msdn.microsoft.com/f2e4144f-f2f1-49db-bfdf-ffce3023b4cb">Using a Pen to Draw Lines and Rectangles</a>
 

 

