---
UID: NF:gdiplusheaders.Region.GetRegionScans(IN const Matrix,OUT Rect,OUT INT)
title: Region::GetRegionScans(IN const Matrix,OUT Rect,OUT INT) (gdiplusheaders.h)
description: The Region::GetRegionScans method gets an array of rectangles that approximate this region. The region is transformed by a specified matrix before the rectangles are calculated.
old-location: gdiplus\_gdiplus_CLASS_Region_GetRegionScans_Matrix_matrix_Rect_rects_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regiongetregionscansmethods\getregionscans.htm
ms.date: 12/05/2018
ms.keywords: GetRegionScans, GetRegionScans method [GDI+], GetRegionScans method [GDI+],Region class, Region class [GDI+],GetRegionScans method, Region.GetRegionScans, Region.GetRegionScans(IN const Matrix,OUT Rect,OUT INT), Region.GetRegionScans(const Matrix*,Rect*,INT*), Region::GetRegionScans, Region::GetRegionScans(IN const Matrix,OUT Rect,OUT INT), _gdiplus_CLASS_Region_GetRegionScans_Matrix_matrix_Rect_rects_INT_count_, gdiplus._gdiplus_CLASS_Region_GetRegionScans_Matrix_matrix_Rect_rects_INT_count_
f1_keywords:
- gdiplusheaders/Region.GetRegionScans
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Region::GetRegionScans(IN const Matrix,OUT Rect,OUT INT)


## -description


The <b>Region::GetRegionScans</b> method gets an array of rectangles that approximate this region. The region is transformed by a specified matrix before the rectangles are calculated.


## -parameters




### -param matrix [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that is used to transform the region. 


### -param rects [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>*</b>

Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a> objects that receives the rectangles. 


### -param count [out]

Type: <b>INT*</b>

Pointer to an 
					INT that receives a value that indicates the number of rectangles that approximate this region. The value is valid even if 
					<i>rects</i> is a <b>NULL</b> pointer. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-region-getregionscanscount">Region::GetRegionScansCount</a> method can be used first to determine the number of rectangles. Then, you can allocate a buffer that is the correct size and set the 
				<i>rects</i> parameter to point to the buffer.


#### Examples



The following example creates a region from a path and gets a set of rectangles that approximate the region. The code then draws each of the rectangles.


```cpp
VOID Example_GetRegionScansRect(HDC hdc)
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
   Region pathRegion(&path);    
   graphics.FillRegion(&solidBrush, &pathRegion);

   // Get the rectangles.
   graphics.GetTransform(&matrix);
   count = pathRegion.GetRegionScansCount(&matrix);
   rects = (Rect*)malloc(count*sizeof(Rect));
   pathRegion.GetRegionScans(&matrix, rects, &count);  

   // Draw the rectangles.
   for(INT j = 0; j < count; ++j)
      graphics.DrawRectangle(&pen, rects[j]);

   free(rects);
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-hit-testing-with-a-region-use">Hit Testing with a Region</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-region-getregionscanscount">Region::GetRegionScansCount</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-regions-about">Regions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
 

 

