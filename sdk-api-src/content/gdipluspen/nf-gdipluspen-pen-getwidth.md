---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# Pen::GetWidth


## -description


The <b>Pen::GetWidth</b> method gets the width currently set for this 
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object.


## -parameters






## -returns



Type: <strong>Type: <b>REAL</b>
</strong>

This method returns a real number that indicates the width of this 
						<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object.




## -remarks



If you pass the address of a pen to one of the draw methods of a 
				<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object, the width of the pen's stroke is dependent on the unit of measure specified in the 
				<b>Graphics</b> object. The default unit of measure is UnitPixel, which is an element of the 
				<a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">Unit</a> enumeration.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object with a specified width and draws a line. The code then gets the width of the pen, creates a second pen based on the width of the first pen, and draws a second line.

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




<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/f86b8bdd-127c-4dc4-88c2-8a1b6fec19bf">Pen::SetWidth</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/b529ba0b-1786-4925-88bd-1a8369fc368c">Setting Pen Width and Alignment</a>
 

 

