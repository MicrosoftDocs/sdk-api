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

# Region::GetRegionScansCount


## -description


The <b>Region::GetRegionScansCount</b> method gets the number of rectangles that approximate this region. The region is transformed by a specified matrix before the rectangles are calculated.


## -parameters




### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Pointer to a matrix that is used to transform the region. 


## -returns



Type: <strong>Type: <b>UINT</b>
</strong>

This method returns an integer that indicates the number of rectangles that approximate this region.




## -remarks



The <b>Region::GetRegionScansCount</b> method can be used before the <a href="https://msdn.microsoft.com/8a9bfbef-9a9c-40f8-9262-62691ae4362d">GetRegionScans</a> method to determine the number of rectangles. Then, you can allocate a buffer that is the correct size to store the rectangles that are obtained with the GetRegionScans method.


#### Examples



The following example creates a region from a path and gets a set of rectangles that approximate the region. The code then draws each of the rectangles.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetRegionScansCount(HDC hdc)
{
   Graphics graphics(hdc);

   SolidBrush solidBrush(Color(255, 255, 0, 0));
   Pen pen(Color(255, 0, 0, 0));
   GraphicsPath path;
   Matrix matrix;
   RectF* rects = NULL;
   INT count = 0;  

   // Create a region from a path.
   path.AddEllipse(10, 10, 50, 300);
   Region pathRegion(&amp;path);    
   graphics.FillRegion(&amp;solidBrush, &amp;pathRegion);

   // Get the rectangles.
   graphics.GetTransform(&amp;matrix);
   count = pathRegion.GetRegionScansCount(&amp;matrix);
   rects = (RectF*)malloc(count*sizeof(RectF));
   pathRegion.GetRegionScans(&amp;matrix, rects, &amp;count);
    
   // Draw the rectangles.
   for(INT j = 0; j &lt; count; ++j)
      graphics.DrawRectangle(&amp;pen, rects[j]);

   free(rects);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">Rect</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn915769">Region</a>



<a href="https://msdn.microsoft.com/8a9bfbef-9a9c-40f8-9262-62691ae4362d">Region::GetRegionScans Methods</a>
 

 

