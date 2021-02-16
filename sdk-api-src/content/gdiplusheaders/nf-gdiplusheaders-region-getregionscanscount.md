---
UID: NF:gdiplusheaders.Region.GetRegionScansCount
title: Region::GetRegionScansCount (gdiplusheaders.h)
description: The Region::GetRegionScansCount method gets the number of rectangles that approximate this region. The region is transformed by a specified matrix before the rectangles are calculated.
helpviewer_keywords: ["GetRegionScansCount","GetRegionScansCount method [GDI+]","GetRegionScansCount method [GDI+]","Region class","Region class [GDI+]","GetRegionScansCount method","Region.GetRegionScansCount","Region::GetRegionScansCount","_gdiplus_CLASS_Region_GetRegionScansCount_matrix_","gdiplus._gdiplus_CLASS_Region_GetRegionScansCount_matrix_"]
old-location: gdiplus\_gdiplus_CLASS_Region_GetRegionScansCount_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\getregionscanscount.htm
ms.date: 12/05/2018
ms.keywords: GetRegionScansCount, GetRegionScansCount method [GDI+], GetRegionScansCount method [GDI+],Region class, Region class [GDI+],GetRegionScansCount method, Region.GetRegionScansCount, Region::GetRegionScansCount, _gdiplus_CLASS_Region_GetRegionScansCount_matrix_, gdiplus._gdiplus_CLASS_Region_GetRegionScansCount_matrix_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Region::GetRegionScansCount
 - gdiplusheaders/Region::GetRegionScansCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Region.GetRegionScansCount
---

# Region::GetRegionScansCount


## -description

The <b>Region::GetRegionScansCount</b> method gets the number of rectangles that approximate this region. The region is transformed by a specified matrix before the rectangles are calculated.

## -parameters

### -param matrix [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Pointer to a matrix that is used to transform the region.

## -returns

Type: <b>UINT</b>

This method returns an integer that indicates the number of rectangles that approximate this region.

## -remarks

The <b>Region::GetRegionScansCount</b> method can be used before the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-region-getregionscans(inconstmatrix_outrect_outint)">GetRegionScans</a> method to determine the number of rectangles. Then, you can allocate a buffer that is the correct size to store the rectangles that are obtained with the GetRegionScans method.


#### Examples



The following example creates a region from a path and gets a set of rectangles that approximate the region. The code then draws each of the rectangles.


```cpp
VOID Example_GetRegionScansCount(HDC hdc)
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
   Region pathRegion(&path);    
   graphics.FillRegion(&solidBrush, &pathRegion);

   // Get the rectangles.
   graphics.GetTransform(&matrix);
   count = pathRegion.GetRegionScansCount(&matrix);
   rects = (RectF*)malloc(count*sizeof(RectF));
   pathRegion.GetRegionScans(&matrix, rects, &count);
    
   // Draw the rectangles.
   for(INT j = 0; j < count; ++j)
      graphics.DrawRectangle(&pen, rects[j]);

   free(rects);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-region-getregionscans(inconstmatrix_outrect_outint)">Region::GetRegionScans Methods</a>