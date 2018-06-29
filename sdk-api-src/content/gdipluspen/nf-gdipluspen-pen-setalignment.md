---
UID: NF:gdipluspen.Pen.SetAlignment
title: Pen::SetAlignment
author: windows-sdk-content
description: The Pen::SetAlignment method sets the alignment for this Pen object relative to the line.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetAlignment_penAlignment_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setalignment.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Pen class [GDI+],SetAlignment method, Pen.SetAlignment, Pen::SetAlignment, SetAlignment, SetAlignment method [GDI+], SetAlignment method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetAlignment_penAlignment_, gdiplus._gdiplus_CLASS_Pen_SetAlignment_penAlignment_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WmfPlaceableFileHeader
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Pen::SetAlignment


## -description


The <b>Pen::SetAlignment</b> method sets the alignment for this 
			<a href="https://msdn.microsoft.com/library/ms534485(v=VS.85).aspx">Pen</a> object relative to the line.


## -parameters




### -param penAlignment [in]

Type: <b><a href="https://msdn.microsoft.com/library/ms534164(v=VS.85).aspx">PenAlignment</a></b>

Element of the <a href="https://msdn.microsoft.com/library/ms534164(v=VS.85).aspx">PenAlignment</a> enumeration that specifies the alignment setting of the pen relative to the line that is drawn. The default value is <b>PenAlignmentCenter</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



If you set the alignment of a 
				<a href="https://msdn.microsoft.com/library/ms534485(v=VS.85).aspx">Pen</a> object to <b>PenAlignmentInset</b>, you cannot use that pen to draw compound lines or triangular dash caps.


#### Examples



The following example creates two 
						<a href="https://msdn.microsoft.com/library/ms534485(v=VS.85).aspx">Pen</a> objects and sets the alignment for one of the pens. The code then draws two lines using each of the pens.

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




<a href="https://msdn.microsoft.com/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/library/ms535017(v=VS.85).aspx">Pen::GetAlignment</a>



<a href="https://msdn.microsoft.com/library/ms534164(v=VS.85).aspx">PenAlignment</a>



<a href="https://msdn.microsoft.com/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/library/ms533854(v=VS.85).aspx">Setting Pen Width and Alignment</a>
 

 

