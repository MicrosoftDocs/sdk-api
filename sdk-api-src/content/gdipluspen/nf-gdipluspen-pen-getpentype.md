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

# Pen::GetPenType


## -description


The <b>Pen::GetPenType</b> method gets the type currently set for this 
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/653472d3-f865-4d20-bc1a-d765d253ecbe">PenType</a></b>
</strong>

This method returns an element of the 
						<a href="https://msdn.microsoft.com/653472d3-f865-4d20-bc1a-d765d253ecbe">PenType</a> enumeration that indicates the style of pen currently set for this 
						<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object.




## -remarks



A 
				<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object is created with a default pen type of <b>PenTypeSolidColor</b>, which is an element of the 
				<a href="https://msdn.microsoft.com/653472d3-f865-4d20-bc1a-d765d253ecbe">PenType</a> enumeration.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/6e633cb2-8b0f-4b6a-95d8-f494d5f972eb">HatchBrush</a> object and then passes the address of that 
						<b>HatchBrush</b> object to a 
						<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> constructor. The code uses the pen, which has a width of 15, to draw a line. The code calls the <b>Pen::GetPenType</b> method to determine the pen's type, and then checks to see whether the type is PenTypeHatchFill.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetPenType(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a HatchBrush object.
   HatchBrush hatchBrush(
      HatchStyleVertical,
      Color(255, 255, 0, 0),
      Color(255, 0, 0, 255));

   // Create a pen based on a hatch brush, and use that
   // pen to draw a line.
   Pen pen(&amp;hatchBrush, 15);
   graphics.DrawLine(&amp;pen, 20, 20, 200, 100);

   // Obtain information about the pen.
   PenType penType = pen.GetPenType();

   if(penType == PenTypeHatchFill)
   {
      // The pen will draw with a hatch pattern.
   }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/15af171c-2966-4b1c-a14f-5d7f2bc6bd95">Pen::GetBrush</a>



<a href="https://msdn.microsoft.com/9a86d978-4339-445e-9595-7a54bdc866dd">Pen::SetBrush</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/f2e4144f-f2f1-49db-bfdf-ffce3023b4cb">Using a Pen to Draw Lines and Rectangles</a>
 

 

