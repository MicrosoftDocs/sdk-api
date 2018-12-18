---
UID: NF:gdipluslinecaps.AdjustableArrowCap.SetMiddleInset
title: AdjustableArrowCap::SetMiddleInset
author: windows-sdk-content
description: The AdjustableArrowCap::SetMiddleInset method sets the number of units that the midpoint of the base shifts towards the vertex.
old-location: gdiplus\_gdiplus_CLASS_AdjustableArrowCap_SetMiddleInset_middleInset_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\adjustablearrowcapclass\adjustablearrowcapmethods\setmiddleinset.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AdjustableArrowCap class [GDI+],SetMiddleInset method, AdjustableArrowCap.SetMiddleInset, AdjustableArrowCap::SetMiddleInset, SetMiddleInset, SetMiddleInset method [GDI+], SetMiddleInset method [GDI+],AdjustableArrowCap class, _gdiplus_CLASS_AdjustableArrowCap_SetMiddleInset_middleInset_, gdiplus._gdiplus_CLASS_AdjustableArrowCap_SetMiddleInset_middleInset_
ms.topic: method
req.header: gdipluslinecaps.h
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
 - AdjustableArrowCap.SetMiddleInset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# AdjustableArrowCap::SetMiddleInset


## -description


The <b>AdjustableArrowCap::SetMiddleInset</b> method sets the number of units that the midpoint of the base shifts towards the vertex.


## -parameters




### -param middleInset [in]

Type: <b>REAL</b>

Real number that specifies the number of units that the midpoint of the base shifts towards the vertex. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<b>Status</b> enumeration.




## -remarks



The middle inset is the number of units that the midpoint of the base shifts towards the vertex. A middle inset of zero results in no shift — the base is a straight line, giving the arrow a triangular shape. A positive (greater than zero) middle inset results in a shift the specified number of units toward the vertex — the base is an arrow shape that points toward the vertex, giving the arrow cap a V-shape. A negative (less than zero) middle inset results in a shift the specified number of units away from the vertex — the base becomes an arrow shape that points away from the vertex, giving the arrow either a diamond shape (if the absolute value of the middle inset is equal to the height) or distorted diamond shape. If the middle inset is equal to or greater than the height of the arrow cap, the cap does not appear at all. The value of the middle inset affects the arrow cap only if the arrow cap is filled. The middle inset defaults to zero when an 
				<b>AdjustableArrowCap</b> object is constructed.


#### Examples



The following example creates an 
						<b>AdjustableArrowCap</b> object, 
						<i>myArrow</i>, and sets the middle inset of the cap to 5 pixels. The code then creates a 
						<b>Pen</b> object and assigns 
						<i>myArrow</i> as the ending line cap for this 
						<b>Pen</b> object. Next, the code draws a capped line.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetMiddleInset(HDC hdc)
{
   Graphics graphics(hdc);

   // Create an AdjustableArrowCap, and set the middle inset to 5.
   AdjustableArrowCap myArrow(10, 10, true);
   myArrow.SetMiddleInset(5.0f);

   // Create a Pen, and assign myArrow as the end cap.
   Pen arrowPen(Color(255, 0, 0, 0));
   arrowPen.SetCustomEndCap(&amp;myArrow);

   // Draw a line using arrowPen.
   graphics.DrawLine(&amp;arrowPen, Point(0, 0), Point(100, 100));
}</pre>
</td>
</tr>
</table></span></div>


