---
UID: NF:gdiplustypes.RectF.Union
title: RectF::Union
author: windows-sdk-content
description: The RectF::Union method determines the union of two rectangles and stores the result in a RectF object.
old-location: gdiplus\_gdiplus_CLASS_RectF_Union_c_a_b_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectfclass\rectfmethods\union_81c_a_b.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: RectF class [GDI+],Union method, RectF.Union, RectF::Union, Union, Union method [GDI+], Union method [GDI+],RectF class, _gdiplus_CLASS_RectF_Union_c_a_b_, gdiplus._gdiplus_CLASS_RectF_Union_c_a_b_
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
 - RectF.Union
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# RectF::Union


## -description


The <b>RectF::Union</b> method determines the union of two rectangles and stores the result in a 
			<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a> object. 


## -parameters




### -param c [out]

Type: <b>RectF&amp;</b>

Reference to a 
					<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a> object that receives the union of the two rectangles. 


### -param a [in]

Type: <b>const RectF&amp;</b>

Reference to one of the two rectangles used to form the union. 


### -param b [in]

Type: <b>const RectF&amp;</b>

Reference to one of the two rectangles used to form the union. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the union of two rectangles is not empty, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -remarks



In GDI+, the union of two rectangles is the smallest rectangle that encloses the two rectangles. A rectangle is defined as empty if its width or height is less than or equal to zero.


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

   // Create three RectF objects.
   RectF rectA(50, 50, 200, 100);
   RectF rectB(70, 20, 100, 200);
   RectF rectC;

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
   graphics.DrawRectangle(&amp;blackPen, rectB);}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/4b57bc29-cec2-4a66-9227-6a31d8f1d4de">Intersect Methods</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">Rect</a>



<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a>



<a href="https://msdn.microsoft.com/f2e4144f-f2f1-49db-bfdf-ffce3023b4cb">Using a Pen to Draw Lines and Rectangles</a>
 

 

