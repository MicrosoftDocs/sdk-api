---
UID: NF:gdipluspath.GraphicsPathIterator.NextMarker(INT,INT)
title: GraphicsPathIterator::NextMarker
description: The GraphicsPathIterator::NextMarker method gets the starting index and the ending index of a section.
tech.root: gdiplus
helpviewer_keywords: ["GraphicsPathIterator::NextMarker"]
ms.assetid: 42272823-7990-4c6e-bb47-4065f568d4bd
ms.date: 05/13/2019
ms.keywords: GraphicsPathIterator::NextMarker
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
 - GraphicsPathIterator::NextMarker
 - gdipluspath/GraphicsPathIterator::NextMarker
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPathIterator::NextMarker
---

# GraphicsPathIterator::NextMarker


## -description

The **GraphicsPathIterator::NextMarker** method gets the starting index and the ending index of the next marker-delimited section in this iterator's associated path.

## -parameters

### -param startIndex

Pointer to an **INT** that receives the starting index.

### -param endIndex

Pointer to an **INT** that receives the ending index.

## -returns

This method returns the number of data points in the retrieved section.
If there are no more marker-delimited sections to retrieve, this method returns 0.

## -remarks

A path has an array of data points that define its lines and curves.
You can call a path's **SetMarker** method to designate certain points in the array as markers.
Those marker points divide the path into sections.

The first time you call the **GraphicsPathIterator::NextMarker** method of an iterator, it gets the first marker-delimited section of that iterator's associated path.
The second time, it gets the second section, and so on.
Each time you call **GraphicsPathIterator::NextSubpath**, it returns the number of data points in the retrieved section.
When there are no sections remaining, it returns 0.

#### Examples

The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object and adds five figures to the path.
The calls to the **SetMarker** method place two markers in the path.
The first marker is at the end of a figure, and the second marker is in the middle of a figure.
The code passes the address of the GraphicsPath object to a **GraphicsPathIterator** constructor to create an iterator that is associated with the path.
Then the code calls the iterator's **GraphicsPathIterator::NextMarker** method twice to obtain the starting and ending indices of the second marker-delimited section of the path.
Finally, the code draws the data points that belong to the second marker-delimited section of the path.

```cpp
VOID NextMarkerExample2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a graphics path with five figures (subpaths).
   GraphicsPath path;

   path.AddRectangle(Rect(20, 20, 60, 30));

   path.SetMarker();                          // first marker
   path.AddLine(100, 20, 160, 50);
   path.AddArc(180, 20, 60, 30, 0, 180);

   path.AddRectangle(Rect(260, 20, 60, 30));
   path.AddLine(340, 20, 400, 50);
   path.SetMarker();                          // second marker
   path.AddArc(340, 20, 60, 30, 0, 180);
   path.CloseFigure();
  
   path.AddRectangle(Rect(420, 20, 60, 30));

   // Create an iterator, and associate it with the path.
   GraphicsPathIterator iterator(&path);

   // Get the second marker-delimited section by calling NextMarker twice.
   INT start;
   INT end;
   INT count;
   count = iterator.NextMarker(&start, &end);
   count = iterator.NextMarker(&start, &end);

   // Get the data points of the second marker-delimited section.
   PointF* points = new PointF[count];
   BYTE* types = new BYTE[count];
   iterator.CopyData(points, types, start, end);

   // Draw the data points of the second marker-delimited section.
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

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextmarker(outconstgraphicspath)">GraphicsPathIterator::NextMarker Methods</a>

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-copydata">GraphicsPathIterator::CopyData</a>

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextmarker(outconstgraphicspath)">GraphicsPathIterator::NextMarker Methods</a>

<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>