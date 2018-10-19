---
UID: NF:gdiplusheaders.Region.GetRegionScansCount
title: Region::GetRegionScansCount
author: windows-sdk-content
description: The Region::GetRegionScansCount method gets the number of rectangles that approximate this region. The region is transformed by a specified matrix before the rectangles are calculated.
old-location: gdiplus\_gdiplus_CLASS_Region_GetRegionScansCount_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\getregionscanscount.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetRegionScansCount, GetRegionScansCount method [GDI+], GetRegionScansCount method [GDI+],Region class, Region class [GDI+],GetRegionScansCount method, Region.GetRegionScansCount, Region::GetRegionScansCount, _gdiplus_CLASS_Region_GetRegionScansCount_matrix_, gdiplus._gdiplus_CLASS_Region_GetRegionScansCount_matrix_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Region.GetRegionScansCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
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



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/2972b879-7d2f-4cad-b17d-670125f43691">Region</a>



<a href="https://msdn.microsoft.com/8a9bfbef-9a9c-40f8-9262-62691ae4362d">Region::GetRegionScans Methods</a>
 

 

