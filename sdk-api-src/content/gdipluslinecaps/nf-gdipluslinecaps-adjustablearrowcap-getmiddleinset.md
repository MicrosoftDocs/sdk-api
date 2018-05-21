---
UID: NF:gdipluslinecaps.AdjustableArrowCap.GetMiddleInset
title: AdjustableArrowCap::GetMiddleInset
author: windows-driver-content
description: The AdjustableArrowCap::GetMiddleInset method gets the value of the inset. The middle inset is the number of units that the midpoint of the base shifts towards the vertex.
old-location: gdiplus\_gdiplus_CLASS_AdjustableArrowCap_GetMiddleInset_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\adjustablearrowcapclass\adjustablearrowcapmethods\getmiddleinset.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: AdjustableArrowCap class [GDI+],GetMiddleInset method, AdjustableArrowCap.GetMiddleInset, AdjustableArrowCap::GetMiddleInset, GetMiddleInset, GetMiddleInset method [GDI+], GetMiddleInset method [GDI+],AdjustableArrowCap class, _gdiplus_CLASS_AdjustableArrowCap_GetMiddleInset_, gdiplus._gdiplus_CLASS_AdjustableArrowCap_GetMiddleInset_
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	AdjustableArrowCap.GetMiddleInset
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# AdjustableArrowCap::GetMiddleInset


## -description


The <b>AdjustableArrowCap::GetMiddleInset</b> method gets the value of the inset. The middle inset is the number of units that the midpoint of the base shifts towards the vertex.


## -parameters






## -returns



Type: <strong>Type: <b>REAL</b>
</strong>

This method returns the inset value.




## -remarks



The middle inset is the number of units that the midpoint of the base shifts towards the vertex. A middle inset of zero results in no shift — the base is a straight line, giving the arrow a triangular shape. A positive (greater than zero) middle inset results in a shift the specified number of units toward the vertex — the base is an arrow shape that points toward the vertex, giving the arrow cap a V-shape. A negative (less than zero) middle inset results in a shift the specified number of units away from the vertex — the base becomes an arrow shape that points away from the vertex, giving the arrow either a diamond shape (if the absolute value of the middle inset is equal to the height) or distorted diamond shape. If the middle inset is equal to or greater than the height of the arrow cap, the cap does not appear at all. The value of the middle inset affects the arrow cap only if the arrow cap is filled. The middle inset defaults to zero when an 
				<b>AdjustableArrowCap</b> object is constructed.


#### Examples




			The following example creates an 
						<b>AdjustableArrowCap</b> object, 
						<i>myArrow</i>, with middle inset set to zero (default value). The code then creates a 
						<b>Pen</b> object, assigns 
						<i>myArrow</i> as the ending line cap for this 
						<b>Pen</b> object, and draws a capped line. Next, the code gets the middle inset, increments it, and draws another capped line.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetMiddleInset(HDC hdc)
{
   Graphics graphics(hdc);

   // Create an AdjustableArrowCap with width and height set to 10. 
   // Middle inset defaults to 0 pixels.
   AdjustableArrowCap myArrow(10, 10, true);

   // Create a Pen, and assign myArrow as the end cap.
   Pen arrowPen(Color(255, 0, 0, 0));
   arrowPen.SetCustomEndCap(&amp;myArrow);

   // Draw a line using arrowPen.
   graphics.DrawLine(&amp;arrowPen, Point(0, 10), Point(100, 10));

   // Get the inset of the arrow.
   REAL inset = myArrow.GetMiddleInset();

   // Increase inset by 5 pixels and draw another line.
   myArrow.SetMiddleInset(inset + 5);
   arrowPen.SetCustomEndCap(&amp;myArrow);
   graphics.DrawLine(&amp;arrowPen, Point(0, 40), Point(100, 40));
}</pre>
</td>
</tr>
</table></span></div>


