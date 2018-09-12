---
UID: NF:gdiplustypes.Rect.Union
title: Rect::Union
author: windows-sdk-content
description: The Rect::Union method determines the union of two rectangles and stores the result in a Rect object.
old-location: gdiplus\_gdiplus_CLASS_Rect_Union_c_a_b_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectclass\rectmethods\union.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Rect class [GDI+],Union method, Rect.Union, Rect::Union, Union, Union method [GDI+], Union method [GDI+],Rect class, _gdiplus_CLASS_Rect_Union_c_a_b_, gdiplus._gdiplus_CLASS_Rect_Union_c_a_b_
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
 - Rect.Union
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Rect::Union


## -description


The <b>Rect::Union</b> method determines the union of two rectangles and stores the result in a 
			<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a> object. 


## -parameters




### -param c [out]

Type: <b>Rect&amp;</b>

Reference to a 
					<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a> object that receives the union of the two rectangles. 


### -param a [in]

Type: <b>const Rect&amp;</b>

Reference to one of the two rectangles used to form the union. 


### -param b [in]

Type: <b>const Rect&amp;</b>

Reference to one of the two rectangles used to form the union. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the union of two rectangles is not empty, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>. 




## -remarks



In Windows GDI+, the union of two rectangles is the smallest rectangle that encloses the two rectangles. A rectangle is defined as empty if its width or height is less than or equal to zero.


#### Examples



The following example creates three rectangles. The code forms the union of the first two rectangles and stores the result in the third rectangle. The code determines whether the union is nonempty and, if so, draws the union.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_UnionABC(HDC hdc)
{
   Graphics graphics(hdc);
   Pen* pGreenPen;

   // Create three Rect objects.
   Rect rectA(50, 50, 200, 100);
   Rect rectB(70, 20, 100, 200);
   Rect rectC;

   // Determine the union of rectA and rectB, and store the result in rectC.
   if(rectC.Union(rectC, rectA, rectB))
   {
      // rectC is not empty.
      // Draw the union with a thick green pen.
      pGreenPen = new Pen(Color(255, 0, 255, 0), 7);
      graphics.DrawRectangle(pGreenPen, rectC);
      delete pGreenPen;
   }
   // Draw rectA and rectB with a thin black pen.
   Pen blackPen(Color(255, 0, 0, 0), 1);
   graphics.DrawRectangle(&amp;blackPen, rectA);
   graphics.DrawRectangle(&amp;blackPen, rectB);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b391c256-5165-4c5c-a45a-dee74e32d391">Intersect Methods</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a>



<a href="https://msdn.microsoft.com/f2e4144f-f2f1-49db-bfdf-ffce3023b4cb">Using a Pen to Draw Lines and Rectangles</a>
 

 

