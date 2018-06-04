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

# PathGradientBrush::GetCenterColor


## -description


The <b>PathGradientBrush::GetCenterColor</b> method gets the color of the center point of this path gradient brush.


## -parameters




### -param color [out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> object that receives the color of the center point. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



By default, the center point of a 
				<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>
 object is the centroid of the brush's boundary path, but you can set the center point to any location, inside or outside the path, by calling the 
				<a href="https://msdn.microsoft.com/41765887-b1de-4259-95af-a1ef8c84d01a">PathGradientBrush::SetCenterPoint Methods</a> method of the 
				<b>PathGradientBrush</b>
 object.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>
 object and uses it to fill an ellipse. Then the code calls the <b>PathGradientBrush::GetCenterColor</b> method of the 
						<b>PathGradientBrush</b>
 object to obtain the center color.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetCenterColor(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(0, 0, 200, 100);

   // Use the path to construct a brush.
   PathGradientBrush pthGrBrush(&amp;path);

   // Set the color at the center of the path to blue.
   pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

   // Set the color along the entire boundary of the path to aqua.
   Color colors[] = {Color(255, 0, 255, 255)};
   int count = 1;
   pthGrBrush.SetSurroundColors(colors, &amp;count);

   // Fill the ellipse with the path gradient brush.
   graphics.FillEllipse(&amp;pthGrBrush, 0, 0, 200, 100);

   // Obtain information about the path gradient brush.
   Color color;
   pthGrBrush.GetCenterColor(&amp;color);

   // Fill a rectangle with the retrieved color.
   SolidBrush solidBrush(color);
   graphics.FillRectangle(&amp;solidBrush, 0, 120, 200, 30);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/6bd4993d-2401-4070-be0e-dbac684095d3">PathGradientBrush::GetCenterPoint Methods</a>



<a href="https://msdn.microsoft.com/33e9a8f0-7c07-475d-8332-cf2e08190b35">PathGradientBrush::SetCenterColor</a>



<a href="https://msdn.microsoft.com/41765887-b1de-4259-95af-a1ef8c84d01a">PathGradientBrush::SetCenterPoint Methods</a>
 

 

