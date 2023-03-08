---
UID: NF:gdiplusheaders.Region.GetRegionScans(constMatrix,RectF,INT)
title: Region::GetRegionScans
description: The Region::GetRegionScans method gets an array of rectangles that approximate this region.
tech.root: gdiplus
helpviewer_keywords: ["Region::GetRegionScans"]
ms.assetid: 0bfb4eed-80f8-4a98-a264-1f47c60f58b8
ms.date: 05/20/2019
ms.keywords: Region::GetRegionScans
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdiplusheaders.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - Region::GetRegionScans
 - gdiplusheaders/Region::GetRegionScans
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - Region::GetRegionScans
---

# Region::GetRegionScans(Matrix*,RectF*,INT*)


## -description

The **Region::GetRegionScans** method gets an array of rectangles that approximate this region.
The region is transformed by a specified matrix before the rectangles are calculated.

## -parameters

### -param matrix

Pointer to a <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that is used to transform the region.

### -param rects

Pointer to an array of <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a> objects that receives the rectangles.

### -param count

Pointer to an **INT** that receives a value that indicates the number of rectangles that approximate this region.
The value is valid even if **rects** is a **NULL** pointer.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The **Region::GetRegionScansCount** method can be used first to determine the number of rectangles.
Then, you can allocate a buffer that is the correct size and set the *rects* parameter to point to the buffer.

#### Examples

The following example creates a region from a path and gets a set of rectangles that approximate the region.
The code then draws each of the rectangles.

```cpp
VOID Example_GetRegionScansRectF(HDC hdc)
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

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>

<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>

<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>

<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-region-getregionscanscount">Region::GetRegionScansCount</a>

<a href="/windows/desktop/gdiplus/-gdiplus-hit-testing-with-a-region-use">Hit Testing with a Region</a>

<a href="/windows/desktop/gdiplus/-gdiplus-regions-about">Regions</a>