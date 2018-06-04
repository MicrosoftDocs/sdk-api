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

# Pen::GetAlignment


## -description


The <b>Pen::GetAlignment</b> method gets the alignment currently set for this 
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/b8d750e1-5528-4252-9fef-53ddfdb552fc">PenAlignment</a></b>
</strong>

This method returns an element of the <a href="https://msdn.microsoft.com/b8d750e1-5528-4252-9fef-53ddfdb552fc">PenAlignment</a> enumeration that indicates the current alignment setting for this <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object.




## -remarks



The default value of <a href="https://msdn.microsoft.com/b8d750e1-5528-4252-9fef-53ddfdb552fc">PenAlignment</a> is PenAlignmentCenter. 


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object, sets the alignment, draws a line, and then gets the pen alignment settings.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetAlignment(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object and set its alignment.
   Pen pen(Color(255, 0, 255, 0), 15);
   pen.SetAlignment(PenAlignmentCenter);

   // Draw a line.
   graphics.DrawLine(&amp;pen, 0, 0, 100, 50);

   // Obtain information about the Pen object.
   PenAlignment penAlignment;
   penAlignment = pen.GetAlignment();

   if(penAlignment == PenAlignmentCenter)
      ;  // The pixels will be centered on the theoretical line.
   else if(penAlignment == PenAlignmentInset)
      ;  // The pixels will lie inside the filled area  of the theoretical line.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/76beb896-ed27-4684-8278-1e0fb5d70a86">Pen::SetAlignment</a>



<a href="https://msdn.microsoft.com/b8d750e1-5528-4252-9fef-53ddfdb552fc">PenAlignment</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/b529ba0b-1786-4925-88bd-1a8369fc368c">Setting Pen Width and Alignment</a>
 

 

