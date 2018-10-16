---
UID: NF:gdipluspen.Pen.SetAlignment
title: Pen::SetAlignment
author: windows-sdk-content
description: The Pen::SetAlignment method sets the alignment for this Pen object relative to the line.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetAlignment_penAlignment_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setalignment.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: Pen class [GDI+],SetAlignment method, Pen.SetAlignment, Pen::SetAlignment, SetAlignment, SetAlignment method [GDI+], SetAlignment method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetAlignment_penAlignment_, gdiplus._gdiplus_CLASS_Pen_SetAlignment_penAlignment_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluspen.h
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
 - Pen.SetAlignment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Pen::SetAlignment


## -description


The <b>Pen::SetAlignment</b> method sets the alignment for this 
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object relative to the line.


## -parameters




### -param penAlignment [in]

Type: <b><a href="https://msdn.microsoft.com/b8d750e1-5528-4252-9fef-53ddfdb552fc">PenAlignment</a></b>

Element of the <a href="https://msdn.microsoft.com/b8d750e1-5528-4252-9fef-53ddfdb552fc">PenAlignment</a> enumeration that specifies the alignment setting of the pen relative to the line that is drawn. The default value is <b>PenAlignmentCenter</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



If you set the alignment of a 
				<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object to <b>PenAlignmentInset</b>, you cannot use that pen to draw compound lines or triangular dash caps.


#### Examples



The following example creates two 
						<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> objects and sets the alignment for one of the pens. The code then draws two lines using each of the pens.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetAlignment(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a black and a green pen.
   Pen blackPen(Color(255, 0, 0, 0), 1);
   Pen greenPen(Color(255, 0, 255, 0), 15);

   // Set the alignment of the green pen.
   greenPen.SetAlignment(PenAlignmentInset);

   // Draw two lines using each pen.
   graphics.DrawEllipse(&amp;greenPen, 0, 0, 100, 200);
   graphics.DrawEllipse(&amp;blackPen, 0, 0, 100, 200);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/05d44fd0-2c15-4d6a-acca-42f1cc4c8c3b">Pen::GetAlignment</a>



<a href="https://msdn.microsoft.com/b8d750e1-5528-4252-9fef-53ddfdb552fc">PenAlignment</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/b529ba0b-1786-4925-88bd-1a8369fc368c">Setting Pen Width and Alignment</a>
 

 

