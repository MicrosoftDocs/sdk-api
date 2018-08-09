---
UID: NF:gdipluspen.Pen.SetDashStyle
title: Pen::SetDashStyle
author: windows-sdk-content
description: The Pen::SetDashStyle method sets the dash style for this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetDashStyle_dashStyle_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setdashstyle.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Pen class [GDI+],SetDashStyle method, Pen.SetDashStyle, Pen::SetDashStyle, SetDashStyle, SetDashStyle method [GDI+], SetDashStyle method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetDashStyle_dashStyle_, gdiplus._gdiplus_CLASS_Pen_SetDashStyle_dashStyle_
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
 - Pen.SetDashStyle
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Pen::SetDashStyle


## -description


The <b>Pen::SetDashStyle</b> method sets the dash style for this 
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object.


## -parameters




### -param dashStyle [in]

Type: <b><a href="https://msdn.microsoft.com/d71ab6cf-9d58-4b26-b1b9-37f16537ab41">DashStyle</a></b>

Element of the 
					<a href="https://msdn.microsoft.com/d71ab6cf-9d58-4b26-b1b9-37f16537ab41">DashStyle</a> enumeration that specifies the dash style for this 
					<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



The length of the dashes in a dashed line is dependent on the dash style and the width of the 
				<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object. The length of the space that separates two dashes in a dashed line is equal to the width of the 
				<b>Pen</b> object. 


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object, sets the dash style, and draws a line. The code then resets the dash style, draws a second line, resets dash style again, and draws a third line.

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




<a href="https://msdn.microsoft.com/0e75de3b-1006-4c8f-875c-eeb0782f24b0">Drawing a Custom Dashed Line</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/1a14f07a-77bf-4151-8f6f-133bea071fa1">Pen::GetDashCap</a>



<a href="https://msdn.microsoft.com/27c2e632-3bfa-490e-8624-64d40901a11c">Pen::GetDashOffset</a>



<a href="https://msdn.microsoft.com/c470a560-953e-44ee-85cf-ac0f39ea7908">Pen::GetDashPattern</a>



<a href="https://msdn.microsoft.com/bba50ce3-d466-47a5-acad-7b0d83b41191">Pen::GetDashPatternCount</a>



<a href="https://msdn.microsoft.com/ca90b234-db33-40a0-bfd3-0d7f43e25b2a">Pen::GetDashStyle</a>



<a href="https://msdn.microsoft.com/b2f12b0c-aaf7-4a49-a4bd-f7f96a1f167a">Pen::SetDashCap</a>



<a href="https://msdn.microsoft.com/7d60736d-76e0-47d8-a138-7d9665741f10">Pen::SetDashOffset</a>



<a href="https://msdn.microsoft.com/bfddd867-a2b1-4f2b-9c99-cc2112e13fa0">Pen::SetDashPattern</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>
 

 

