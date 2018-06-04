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

# Pen::SetDashOffset


## -description


The <b>Pen::SetDashOffset</b> method sets the distance from the start of the line to the start of the first dash in a dashed line.


## -parameters




### -param dashOffset [in]

Type: <b>REAL</b>

Real number that specifies the number of times to shift the spaces in a dashed line. Each shift is equal to the length of a space in the dashed line. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



A positive 
				<i>dashOffset</i> value shifts the first dash forward along the path, and a negative 
				<i>dashOffset</i> value shifts the start of the path forward along the first dash. 


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object, sets the dash style, and draws a line. The code then sets the pen's offset value and draws a second line.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetDashOffset(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object, set the dash style, and draw a line.
   Pen pen(Color(255, 0, 0, 255), 15);
   pen.SetDashStyle(DashStyleDash);
   graphics.DrawLine(&amp;pen, 0, 50, 400, 50);

   // Set the dash offset value for the pen, and draw a second line.
   pen.SetDashOffset(10);
   graphics.DrawLine(&amp;pen, 0, 80, 400, 80);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0e75de3b-1006-4c8f-875c-eeb0782f24b0">Drawing a Custom Dashed Line</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/27c2e632-3bfa-490e-8624-64d40901a11c">Pen::GetDashOffset</a>



<a href="https://msdn.microsoft.com/c470a560-953e-44ee-85cf-ac0f39ea7908">Pen::GetDashPattern</a>



<a href="https://msdn.microsoft.com/bba50ce3-d466-47a5-acad-7b0d83b41191">Pen::GetDashPatternCount</a>



<a href="https://msdn.microsoft.com/ca90b234-db33-40a0-bfd3-0d7f43e25b2a">Pen::GetDashStyle</a>



<a href="https://msdn.microsoft.com/b2f12b0c-aaf7-4a49-a4bd-f7f96a1f167a">Pen::SetDashCap</a>



<a href="https://msdn.microsoft.com/bfddd867-a2b1-4f2b-9c99-cc2112e13fa0">Pen::SetDashPattern</a>



<a href="https://msdn.microsoft.com/076c807f-8bdb-4366-bfb3-903b6b872d08">Pen::SetDashStyle</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>
 

 

