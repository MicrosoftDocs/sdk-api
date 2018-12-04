---
UID: NF:gdipluspen.Pen.SetDashCap
title: Pen::SetDashCap
author: windows-sdk-content
description: The Pen::SetDashCap method sets the dash cap style for this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetDashCap_dashCap_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setdashcap.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: Pen class [GDI+],SetDashCap method, Pen.SetDashCap, Pen::SetDashCap, SetDashCap, SetDashCap method [GDI+], SetDashCap method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetDashCap_dashCap_, gdiplus._gdiplus_CLASS_Pen_SetDashCap_dashCap_
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
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object.


## -parameters




### -param dashCap [in]

Type: <b><a href="https://msdn.microsoft.com/8e96f7c2-237e-4172-8e3c-62d47627b430">DashCap</a></b>

Element of the 
					<a href="https://msdn.microsoft.com/8e96f7c2-237e-4172-8e3c-62d47627b430">DashCap</a> enumeration that specifies the dash cap for this 
					<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



If you set the alignment of a 
				<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object to <b>PenAlignmentInset</b>, you cannot use that pen to draw triangular dash caps.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object, sets the dash style and the dash cap, and draws a dashed line.

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




<a href="https://msdn.microsoft.com/0e75de3b-1006-4c8f-875c-eeb0782f24b0">Drawing a Custom Dashed Line</a>



<a href="https://msdn.microsoft.com/c9d90114-3913-486c-a808-b08dd473d9a1">Drawing a Line with Line Caps</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/fcc0c624-d60a-4c77-b7d0-3921f0b49471">Pen::GetCustomEndCap</a>



<a href="https://msdn.microsoft.com/39a64e5c-d82b-4b0e-b851-db42996047a0">Pen::GetCustomStartCap</a>



<a href="https://msdn.microsoft.com/1a14f07a-77bf-4151-8f6f-133bea071fa1">Pen::GetDashCap</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>
 

 

