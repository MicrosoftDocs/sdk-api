---
UID: NF:gdiplusheaders.Region.GetRegionScans(IN const Matrix,OUT Rect,OUT INT)
title: Region::GetRegionScans(IN const Matrix,OUT Rect,OUT INT)
author: windows-sdk-content
description: The Region::GetRegionScans method gets an array of rectangles that approximate this region. The region is transformed by a specified matrix before the rectangles are calculated.
old-location: gdiplus\_gdiplus_CLASS_Region_GetRegionScans_Matrix_matrix_Rect_rects_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regiongetregionscansmethods\getregionscans.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRegionScans, GetRegionScans method [GDI+], GetRegionScans method [GDI+],Region class, Region class [GDI+],GetRegionScans method, Region.GetRegionScans, Region.GetRegionScans(IN const Matrix,OUT Rect,OUT INT), Region.GetRegionScans(const Matrix*,Rect*,INT*), Region::GetRegionScans, Region::GetRegionScans(IN const Matrix,OUT Rect,OUT INT), _gdiplus_CLASS_Region_GetRegionScans_Matrix_matrix_Rect_rects_INT_count_, gdiplus._gdiplus_CLASS_Region_GetRegionScans_Matrix_matrix_Rect_rects_INT_count_
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
 - Region.GetRegionScans
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Region::GetRegionScans(IN const Matrix,OUT Rect,OUT INT)


## -description


The <b>Region::GetRegionScans</b> method gets an array of rectangles that approximate this region. The region is transformed by a specified matrix before the rectangles are calculated.


## -parameters




### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that is used to transform the region. 


### -param rects [out]

Type: <b><a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a> objects that receives the rectangles. 


### -param count [out]

Type: <b>INT*</b>

Pointer to an 
					INT that receives a value that indicates the number of rectangles that approximate this region. The value is valid even if 
					<i>rects</i> is a <b>NULL</b> pointer. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The <a href="https://msdn.microsoft.com/dc210aa9-6af7-4189-ab53-d961c4c57bfc">Region::GetRegionScansCount</a> method can be used first to determine the number of rectangles. Then, you can allocate a buffer that is the correct size and set the 
				<i>rects</i> parameter to point to the buffer.


#### Examples



The following example creates a region from a path and gets a set of rectangles that approximate the region. The code then draws each of the rectangles.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetRegionScansRect(HDC hdc)
{
   Graphics graphics(hdc);

   SolidBrush solidBrush(Color(255, 255, 0, 0));
   Pen pen(Color(255, 0, 0, 0));
   GraphicsPath path;
   Matrix matrix;
   Rect* rects = NULL;
   INT count = 0;  

   // Create a region from a path.
   path.AddEllipse(10, 10, 50, 300);
   Region pathRegion(&amp;path);    
   graphics.FillRegion(&amp;solidBrush, &amp;pathRegion);

   // Get the rectangles.
   graphics.GetTransform(&amp;matrix);
   count = pathRegion.GetRegionScansCount(&amp;matrix);
   rects = (Rect*)malloc(count*sizeof(Rect));
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




<a href="https://msdn.microsoft.com/9776b73e-191e-4a8e-9abe-e485ffed954c">Hit Testing with a Region</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/2972b879-7d2f-4cad-b17d-670125f43691">Region</a>



<a href="https://msdn.microsoft.com/dc210aa9-6af7-4189-ab53-d961c4c57bfc">Region::GetRegionScansCount</a>



<a href="https://msdn.microsoft.com/eb78d7a0-6293-487f-88c5-88ba455b965f">Regions</a>



<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a>
 

 

