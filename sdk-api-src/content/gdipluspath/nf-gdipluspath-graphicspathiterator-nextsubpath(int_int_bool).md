---
UID: NF:gdipluspath.GraphicsPathIterator.NextSubpath(INT,INT,BOOL)
title: GraphicsPathIterator::NextSubpath
description: The GraphicsPathIterator::NextSubpath method gets the starting index and the ending index of the next subpath.
tech.root: gdiplus
helpviewer_keywords: ["GraphicsPathIterator::NextSubpath"]
ms.assetid: 175a664d-76d3-40d7-8978-90120e26baf6
ms.date: 05/13/2019
ms.keywords: GraphicsPathIterator::NextSubpath
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdipluspath.h
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
 - GraphicsPathIterator::NextSubpath
 - gdipluspath/GraphicsPathIterator::NextSubpath
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPathIterator::NextSubpath
---

## -description

The **GraphicsPathIterator::NextSubpath** method gets the starting index and the ending index of the next subpath (figure) in this iterator's associated path.

## -parameters

### -param startIndex

Pointer to an **INT** that receives the starting index.

### -param endIndex

Pointer to an **INT** that receives the ending index.

### -param isClosed

Pointer to a **BOOL** that receives a value that indicates whether the obtained figure is closed.
If the figure is closed, the received value is **TRUE**; otherwise, the received value is **FALSE**.

## -returns

This method returns the number of data points in the next figure.
If there are no more figures in the path, this method returns 0.

## -remarks

The first time you call the **GraphicsPathIterator::NextSubpath** method of an iterator, it gets the indices for the first figure (subpath) of that iterator's associated path.
The second time, it gets the indices for the second figure, and so on.
Each time you call **GraphicsPathIterator::NextSubpath**, it returns the number of data points in the figure whose indices were retrieved.
When there are no figures remaining, it returns 0.

#### Examples

The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object and adds five figures to the path.
The code passes the address of that *GraphicsPath* object to a **GraphicsPathIterator** constructor to create an iterator that is associated with the path. The code calls the iterator's **GraphicsPathIterator::NextSubpath** method three times to obtain the starting index and the ending index of the path's third figure.
Then the code calls the iterator's **GraphicsPathIterator::CopyData** method to retrieve the third figure's data points.

```cpp
VOID NextSubpathExample2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a graphics path with five figures (subpaths).
   GraphicsPath path;

   path.AddRectangle(Rect(20, 20, 60, 30));   // Subpath count is 1.

   path.AddLine(100, 20, 160, 50);            // Subpath count is 2.
   path.AddArc(180, 20, 60, 30, 0.0f, 180.0f);

   path.AddRectangle(Rect(260, 20, 60, 30));  // Subpath count is 3.

   path.AddLine(340, 20, 400, 50);            // Subpath count is 4.
   path.AddArc(340, 20, 60, 30, 0.0f, 180.0f);
   path.CloseFigure();
  
   path.AddRectangle(Rect(420, 20, 60, 30));  // Subpath count is 5.

   // Create an iterator, and associate it with the path.
   GraphicsPathIterator iterator(&path);

   // Call NextSubpath three times to get the starting and ending
   // indices for the third figure.
   INT start;
   INT end;
   BOOL isClosed;
   INT count;
   count = iterator.NextSubpath(&start, &end, &isClosed);
   count = iterator.NextSubpath(&start, &end, &isClosed);
   count = iterator.NextSubpath(&start, &end, &isClosed);

   // Get the third figure's data points.
   PointF* points = new PointF[count];
   BYTE* types = new BYTE[count];
   iterator.CopyData(points, types, start, end);

   // Draw the third figure's data points.
   SolidBrush brush(Color(255, 255, 0, 0));
   for(INT j = 0; j < count; ++j)
      graphics.FillEllipse(
         &brush,
         points[j].X - 3.0f,
         points[j].Y - 3.0f,
         6.0f,
         6.0f);

   delete points;
   delete types;
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathdata">GraphicsPath::GetPathData</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-copydata">GraphicsPathIterator::CopyData</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-getsubpathcount">GraphicsPathIterator::GetSubpathCount</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextmarker(outconstgraphicspath)">GraphicsPathIterator::NextMarker Methods</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextsubpath(outconstgraphicspath_outbool)">NextSubpath</a>

<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>