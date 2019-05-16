---
UID: NF:gdiplusheaders.Region.GetRegionScans
title: Region::GetRegionScans
description: The Region::GetRegionScans method gets an array of rectangles that approximate this region.
ms.assetid: 0bfb4eed-80f8-4a98-a264-1f47c60f58b8
ms.author: windowssdkdev
ms.date: 05/20/2019
ms.keywords: Region::GetRegionScans
ms.topic: language-reference
targetos: Windows
product: Windows
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

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a> object that is used to transform the region.

### -param rects

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a> objects that receives the rectangles.

### -param count

Pointer to an **INT** that receives a value that indicates the number of rectangles that approximate this region.
The value is valid even if **rects** is a **NULL** pointer.

## -returns

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

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

<a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534769(v=VS.85).aspx">Region::GetRegionScansCount</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533826(v=VS.85).aspx">Hit Testing with a Region</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536378(v=VS.85).aspx">Regions</a>
