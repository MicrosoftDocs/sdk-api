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

# Pen::SetDashPattern


## -description


The <b>Pen::SetDashPattern</b> method sets an array of custom dashes and spaces for this 
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object.


## -parameters




### -param dashArray [in]

Type: <b>const REAL*</b>

Pointer to an array of real numbers that specifies the length of the custom dashes and spaces. All elements in the array must be positive real numbers. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>dashArray</i> array. The integer must be greater than 0 and not greater than the total number of elements in the array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



This method will set the 
				<a href="https://msdn.microsoft.com/d71ab6cf-9d58-4b26-b1b9-37f16537ab41">DashStyle</a> enumeration for this 
				<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object to <b>DashStyleCustom</b>. 

The elements in the 
				<i>dashArray</i> array set the length of each dash and space in the dash pattern. The first element sets the length of a dash, the second element sets the length of a space, the third element sets the length of a dash, and so forth.

The length of each dash and space in the dash pattern is the product of the element value in the array and the width of the 
				<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object.


#### Examples



The following example creates an array of real numbers. The code then creates a 
						<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object, sets the dash pattern based on the array, and then draws the custom dashed line.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetDashPattern(HDC hdc)
{
   Graphics graphics(hdc);

   // Create and set an array of real numbers.
   REAL dashVals[4] = {
      5.0f,   // dash length 5
      2.0f,   // space length 2
      15.0f,  // dash length 15
      4.0f};  // space length 4

   // Create a Pen object.
   Pen pen(Color(255, 0, 0, 0), 5);

   // Set the dash pattern for the custom dashed line.
   pen.SetDashPattern(dashVals, 4);

   // Draw the custom dashed line.
   graphics.DrawLine(&amp;pen, 5, 20, 405, 200); 
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0e75de3b-1006-4c8f-875c-eeb0782f24b0">Drawing a Custom Dashed Line</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/c470a560-953e-44ee-85cf-ac0f39ea7908">Pen::GetDashPattern</a>



<a href="https://msdn.microsoft.com/bba50ce3-d466-47a5-acad-7b0d83b41191">Pen::GetDashPatternCount</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>
 

 

