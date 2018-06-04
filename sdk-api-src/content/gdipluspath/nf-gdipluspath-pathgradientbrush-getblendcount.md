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

# PathGradientBrush::GetBlendCount


## -description


The <b>PathGradientBrush::GetBlendCount</b> method gets the number of blend factors currently set for this path gradient brush.


## -parameters






## -returns



Type: <strong>Type: <b>INT</b>
</strong>

This method returns the number of blend factors currently set for this path gradient brush.




## -remarks



Before you call the <a href="https://msdn.microsoft.com/8a4ff6de-615e-4128-9e88-337ed6f4af7f">PathGradientBrush::GetBlend</a> method of a 
				<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>
 object, you must allocate two buffers: one to receive an array of blend factors and one to receive an array of blend positions. To determine the size of the required buffers, call the <b>PathGradientBrush::GetBlendCount</b> method of the 
				<b>PathGradientBrush</b>
 object. The size (in bytes) of each buffer should be the return value of <b>PathGradientBrush::GetBlendCount</b>
 multiplied by 
				<b>sizeof</b>(
				<b>REAL</b>).


#### Examples



The following example demonstrates several methods of the 
						<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>
 class, including <a href="https://msdn.microsoft.com/3abf3b42-d72e-413e-9daf-ba0e8146695e">PathGradientBrush::SetBlend</a>, <b>PathGradientBrush::GetBlendCount</b>
, and <a href="https://msdn.microsoft.com/8a4ff6de-615e-4128-9e88-337ed6f4af7f">PathGradientBrush::GetBlend</a>. The code creates a 
						<b>PathGradientBrush</b>
 object and calls the <b>PathGradientBrush::SetBlend</b> method to establish a set of blend factors and blend positions for the brush. Then the code calls the <b>PathGradientBrush::GetBlendCount</b>
 method to retrieve the number of blend factors. After the number of blend factors is retrieved, the code allocates two buffers: one to receive the array of blend factors and one to receive the array of blend positions. Then the code calls the <b>PathGradientBrush::GetBlend</b> method to retrieve the blend factors and the blend positions.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetBlend(HDC hdc)
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
   INT count = 1;
   pthGrBrush.SetSurroundColors(colors, &amp;count);

   // Set blend factors and positions for the path gradient brush.
   REAL fac[] = {
      0.0f, 
      0.4f,     // 40 percent of the way from aqua to blue
      0.8f,     // 80 percent of the way from aqua to blue
      1.0f};

   REAL pos[] = {
      0.0f, 
      0.3f,   // 30 percent of the way from the boundary to the center
      0.7f,   // 70 percent of the way from the boundary to the center
      1.0f};

   pthGrBrush.SetBlend(fac, pos, 4);

   // Fill the ellipse with the path gradient brush.
   graphics.FillEllipse(&amp;pthGrBrush, 0, 0, 200, 100);

   // Obtain information about the path gradient brush.
   INT blendCount = pthGrBrush.GetBlendCount();
   REAL* factors = new REAL[blendCount];
   REAL* positions = new REAL[blendCount];

   pthGrBrush.GetBlend(factors, positions, blendCount);

   for(INT j = 0; j &lt; blendCount; ++j)
   {
      // Inspect or use the value in factors[j].
      // Inspect or use the value in positions[j].    
   }

   delete [] factors;
   delete [] positions; 
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/8a4ff6de-615e-4128-9e88-337ed6f4af7f">PathGradientBrush::GetBlend</a>



<a href="https://msdn.microsoft.com/3abf3b42-d72e-413e-9daf-ba0e8146695e">PathGradientBrush::SetBlend</a>
 

 

