---
UID: NF:gdiplustypes.RectF.Inflate(IN REAL,IN REAL)
title: RectF::Inflate(IN REAL,IN REAL)
author: windows-sdk-content
description: The RectF::Inflate method expands the rectangle by dx on the left and right edges, and by dy on the top and bottom edges.
old-location: gdiplus\_gdiplus_CLASS_RectF_Inflate_dx_dy_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectfclass\rectfmethods\rectfinflatemethods\inflate_74dx_dy.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: Inflate, Inflate method [GDI+], Inflate method [GDI+],RectF class, RectF class [GDI+],Inflate method, RectF.Inflate, RectF.Inflate(IN REAL,IN REAL), RectF.Inflate(REAL,REAL), RectF::Inflate, RectF::Inflate(IN REAL,IN REAL), _gdiplus_CLASS_RectF_Inflate_dx_dy_, gdiplus._gdiplus_CLASS_RectF_Inflate_dx_dy_
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
 - RectF.Inflate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# RectF::Inflate(IN REAL,IN REAL)


## -description


The <b>RectF::Inflate</b> method expands the rectangle by 
			<i>dx</i> on the left and right edges, and by 
			<i>dy</i> on the top and bottom edges.


## -parameters




### -param dx [in]

Type: <b>REAL</b>

Real number that specifies the amount to expand the rectangle on the left and right edges. 


### -param dy [in]

Type: <b>REAL</b>

Real number that specifies the amount to expand the rectangle on the top and bottom edges. 


## -returns



This method does not return a value.




## -remarks



The x-coordinate of the left edge is decreased by 
				<i>dx</i>, and the x-coordinate of the right edge is increased by 
				<i>dx</i>. The y-coordinate of the top edge is decreased by 
				<i>dy</i> and the y-coordinate of the bottom edge is increased by 
				<i>dy</i>.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a> object, draws the rectangle, inflates the rectangle, and then redraws the rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_InflateDxDy(HDC hdc)
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 0));

   // Create and draw a rectangle.
   RectF rect(100, 100, 80, 40);
   graphics.DrawRectangle(&amp;pen, rect);

   // Inflate the rectangle, and then redraw the rectangle.
   rect.Inflate(20, 10);
   graphics.DrawRectangle(&amp;pen, rect);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a>



<a href="https://msdn.microsoft.com/f2e4144f-f2f1-49db-bfdf-ffce3023b4cb">Using a Pen to Draw Lines and Rectangles</a>
 

 

