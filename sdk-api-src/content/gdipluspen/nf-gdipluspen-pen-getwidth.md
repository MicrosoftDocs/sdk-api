---
UID: NF:gdipluspen.Pen.GetWidth
title: Pen::GetWidth
author: windows-sdk-content
description: The Pen::GetWidth method gets the width currently set for this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_GetWidth_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\getwidth_36.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetWidth, GetWidth method [GDI+], GetWidth method [GDI+],Pen class, Pen class [GDI+],GetWidth method, Pen.GetWidth, Pen::GetWidth, _gdiplus_CLASS_Pen_GetWidth_, gdiplus._gdiplus_CLASS_Pen_GetWidth_
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
 - Pen.GetWidth
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Pen::GetWidth


## -description


The <b>Pen::GetWidth</b> method gets the width currently set for this 
			<a href="https://msdn.microsoft.com/library/ms534485(v=VS.85).aspx">Pen</a> object.


## -parameters






## -returns



Type: <strong>Type: <b>REAL</b>
</strong>

This method returns a real number that indicates the width of this 
						<a href="https://msdn.microsoft.com/library/ms534485(v=VS.85).aspx">Pen</a> object.




## -remarks



If you pass the address of a pen to one of the draw methods of a 
				<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object, the width of the pen's stroke is dependent on the unit of measure specified in the 
				<b>Graphics</b> object. The default unit of measure is UnitPixel, which is an element of the 
				<a href="https://msdn.microsoft.com/library/ms534405(v=VS.85).aspx">Unit</a> enumeration.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/library/ms534485(v=VS.85).aspx">Pen</a> object with a specified width and draws a line. The code then gets the width of the pen, creates a second pen based on the width of the first pen, and draws a second line.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetWidth(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a pen with a width of 15, and 
   // use that pen to draw a line.
   Pen pen(Color(255, 0, 0, 255), 15);
   graphics.DrawLine(&amp;pen, 20, 20, 200, 100);

   // Get the width of the pen.
   REAL width = pen.GetWidth();

   // Create another pen that has the same width.
   Pen pen2(Color(255, 0, 255, 0), width);

   // Draw a second line.
   graphics.DrawLine(&amp;pen2, 20, 60, 200, 140);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/library/ms535057(v=VS.85).aspx">Pen::SetWidth</a>



<a href="https://msdn.microsoft.com/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/library/ms533854(v=VS.85).aspx">Setting Pen Width and Alignment</a>
 

 

