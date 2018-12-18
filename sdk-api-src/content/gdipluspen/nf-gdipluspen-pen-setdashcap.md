---
UID: NF:gdipluspen.Pen.SetDashCap
title: Pen::SetDashCap
author: windows-sdk-content
description: The Pen::SetDashCap method sets the dash cap style for this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetDashCap_dashCap_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setdashcap.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Pen class [GDI+],SetDashCap method, Pen.SetDashCap, Pen::SetDashCap, SetDashCap, SetDashCap method [GDI+], SetDashCap method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetDashCap_dashCap_, gdiplus._gdiplus_CLASS_Pen_SetDashCap_dashCap_
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
 - Pen.SetDashCap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Pen::SetDashCap


## -description


The <b>Pen::SetDashCap</b> method sets the dash cap style for this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object.


## -parameters




### -param dashCap [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534102(v=VS.85).aspx">DashCap</a></b>

Element of the 
					<a href="https://msdn.microsoft.com/en-us/library/ms534102(v=VS.85).aspx">DashCap</a> enumeration that specifies the dash cap for this 
					<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



If you set the alignment of a 
				<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object to <b>PenAlignmentInset</b>, you cannot use that pen to draw triangular dash caps.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object, sets the dash style and the dash cap, and draws a dashed line.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetCustomStartCap(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a pen.
   Pen pen(Color(255, 0, 0, 255), 20);

   // Set the dash style for the pen.
   pen.SetDashStyle(DashStyleDash);

   // Set a triangular dash cap for the pen.
   pen.SetDashCap(DashCapTriangle);

   // Draw a line using the pen.
   graphics.DrawLine(&amp;pen, 20, 20, 200, 100);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533850(v=VS.85).aspx">Drawing a Custom Dashed Line</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533852(v=VS.85).aspx">Drawing a Line with Line Caps</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535022(v=VS.85).aspx">Pen::GetCustomEndCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535023(v=VS.85).aspx">Pen::GetCustomStartCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535024(v=VS.85).aspx">Pen::GetDashCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>
 

 

