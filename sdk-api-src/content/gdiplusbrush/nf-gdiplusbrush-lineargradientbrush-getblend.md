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

# LinearGradientBrush::GetBlend


## -description


The <b>LinearGradientBrush::GetBlend</b> method gets the blend factors and their corresponding blend positions from a 
			<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a> object.


## -parameters




### -param blendFactors [out]

Type: <b>REAL*</b>

Pointer to an array that receives the blend factors. Each number in the array indicates a percentage of the ending color and is in the range from 0.0 through 1.0. 


### -param blendPositions [out]

Type: <b>REAL*</b>

Pointer to an array that receives the blend positions. Each number in the array indicates a percentage of the distance between the starting boundary and the ending boundary and is in the range from 0.0 through 1.0, where 0.0 indicates the starting boundary of the gradient and 1.0 indicates the ending boundary. A blend position between 0.0 and 1.0 indicates a line, parallel to the boundary lines, that is a certain fraction of the distance from the starting boundary to the ending boundary. For example, a blend position of 0.7 indicates the line that is 70 percent of the distance from the starting boundary to the ending boundary. The color is constant on lines that are parallel to the boundary lines. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of blend factors to retrieve. Before calling the <b>LinearGradientBrush::GetBlend</b> method of a 
					<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a> object, call the <a href="https://msdn.microsoft.com/2be97b73-a5dc-44d1-ae4f-bb9c215b3e71">LinearGradientBrush::GetBlendCount</a> method of that same 
					<b>LinearGradientBrush</b> object to determine the current number of blend factors. The number of blend positions retrieved is the same as the number of blend factors retrieved. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



A 
				<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a> object has two parallel boundaries: a starting boundary and an ending boundary. A color is associated with each of these two boundaries. Each boundary is a straight line that passes through a specified point — the starting boundary passes through the starting point; the ending boundary passes through the ending point — and is perpendicular to the direction of the linear gradient brush. The direction of the linear gradient brush follows the line that is defined by the starting and ending points. This line, the "directional line," may be horizontal, vertical, or diagonal. All points that lie on a line that is parallel to the boundaries are the same color. When you fill an area with a linear gradient brush, the color changes gradually from one line to the next as you move along the directional line from the starting boundary to the ending boundary. By default, the change in color is proportional to the change in distance; that is, a line 30 percent of the distance between the starting boundary and the ending boundary has a color that is 30 percent of the distance between the starting boundary color and the ending boundary color. The color pattern is repeated outside of the starting and ending boundaries.

You can call the <a href="https://msdn.microsoft.com/e2b96c7b-083c-47ef-9b29-3ec403f41462">LinearGradientBrush::SetBlend</a> method of a 
				<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a> object to customize the relationship between color and distance. For example, suppose you set the blend positions to {0, 0.5, 1} and you set the blend factors to {0, 0.3, 1}. Then a line 50 percent of the distance between the starting boundary and the ending boundary will have a color that is 30 percent of the distance between the starting boundary color and the ending boundary color.


#### Examples



The following example creates a linear gradient brush, sets its blend, and uses the brush to fill a rectangle. The code then gets the blend. The blend factors and positions can then be inspected or used in some way.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetBlend(HDC hdc)
{
   Graphics myGraphics(hdc);

   // Create a linear gradient brush, and set its blend.
   REAL fac[] = {0.0f, 0.4f, 0.6f, 1.0f};
   REAL pos[] = {0.0f, 0.2f, 0.8f, 1.0f};

   LinearGradientBrush linGrBrush(
      Point(0, 0), 
      Point(100, 0),
      Color(255, 255, 0, 0),   // red
      Color(255, 0, 0, 255));  // blue

   linGrBrush.SetBlend(fac, pos, 4);

   // Use the linear gradient brush to fill a rectangle.
   myGraphics.FillRectangle(&amp;linGrBrush, 0, 0, 100, 50);

   // Obtain information about the linear gradient brush.
   INT   blendCount;
   REAL* factors = NULL;
   REAL* positions = NULL;

   blendCount = linGrBrush.GetBlendCount();
   factors = new REAL[blendCount];
   positions = new REAL[blendCount];

   linGrBrush.GetBlend(factors, positions, blendCount);

   for(INT j = 0; j &lt; blendCount; ++j)
   {
      // Inspect or use the value in factors[j].
      // Inspect or use the value in positions[j].
   }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/e37b4c3a-b753-483a-990f-da3bcc70acf5">Filling Shapes with a Gradient Brush</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/2be97b73-a5dc-44d1-ae4f-bb9c215b3e71">LinearGradientBrush::GetBlendCount</a>



<a href="https://msdn.microsoft.com/e2b96c7b-083c-47ef-9b29-3ec403f41462">LinearGradientBrush::SetBlend</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">Point</a>
 

 

