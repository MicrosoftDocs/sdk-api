---
UID: NF:gdipluspen.Pen.SetDashStyle
title: Pen::SetDashStyle
author: windows-sdk-content
description: The Pen::SetDashStyle method sets the dash style for this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetDashStyle_dashStyle_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setdashstyle.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Pen class [GDI+],SetDashStyle method, Pen.SetDashStyle, Pen::SetDashStyle, SetDashStyle, SetDashStyle method [GDI+], SetDashStyle method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetDashStyle_dashStyle_, gdiplus._gdiplus_CLASS_Pen_SetDashStyle_dashStyle_
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
 - Pen.SetDashStyle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdipluspen.h
: 
- Pen.SetDashStyle
: 
req.product: GDI+ 1.0
---

# Pen::SetDashStyle


## -description


The <b>Pen::SetDashStyle</b> method sets the dash style for this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object.


## -parameters




### -param dashStyle [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534104(v=VS.85).aspx">DashStyle</a></b>

Element of the 
					<a href="https://msdn.microsoft.com/en-us/library/ms534104(v=VS.85).aspx">DashStyle</a> enumeration that specifies the dash style for this 
					<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



The length of the dashes in a dashed line is dependent on the dash style and the width of the 
				<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object. The length of the space that separates two dashes in a dashed line is equal to the width of the 
				<b>Pen</b> object. 


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object, sets the dash style, and draws a line. The code then resets the dash style, draws a second line, resets dash style again, and draws a third line.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetDashStyle(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object.
   Pen pen(Color(255, 0, 0, 255), 15);

   // Set the dash style for the pen, and draw a dashed line.
   pen.SetDashStyle(DashStyleDash);
   graphics.DrawLine(&amp;pen, 0, 50, 400, 150);

   // Reset the dash style for the pen, and draw a second line.
   pen.SetDashStyle(DashStyleDot);
   graphics.DrawLine(&amp;pen, 0, 80, 400, 180); 

   // Reset the dash style for the pen, and draw a third line.
   pen.SetDashStyle(DashStyleDashDot);
   graphics.DrawLine(&amp;pen, 0, 110, 400, 210); 
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533850(v=VS.85).aspx">Drawing a Custom Dashed Line</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535024(v=VS.85).aspx">Pen::GetDashCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535025(v=VS.85).aspx">Pen::GetDashOffset</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535026(v=VS.85).aspx">Pen::GetDashPattern</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535027(v=VS.85).aspx">Pen::GetDashPatternCount</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535028(v=VS.85).aspx">Pen::GetDashStyle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535047(v=VS.85).aspx">Pen::SetDashCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535048(v=VS.85).aspx">Pen::SetDashOffset</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535049(v=VS.85).aspx">Pen::SetDashPattern</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>
 

 

