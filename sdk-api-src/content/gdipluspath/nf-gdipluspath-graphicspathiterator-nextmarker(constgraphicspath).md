---
UID: NF:gdipluspath.GraphicsPathIterator.NextMarker(constGraphicsPath)
title: GraphicsPathIterator::NextMarker(OUT const GraphicsPath) (gdipluspath.h)
description: The GraphicsPathIterator::NextMarker method gets the next marker-delimited section of this iterator's associated path.
helpviewer_keywords: ["GraphicsPathIterator class [GDI+]","NextMarker method","GraphicsPathIterator.NextMarker","GraphicsPathIterator.NextMarker(GraphicsPath*)","GraphicsPathIterator.NextMarker(OUT const GraphicsPath)","GraphicsPathIterator::NextMarker","GraphicsPathIterator::NextMarker(OUT const GraphicsPath)","NextMarker","NextMarker method [GDI+]","NextMarker method [GDI+]","GraphicsPathIterator class","_gdiplus_CLASS_GraphicsPathIterator_NextMarker_path_","gdiplus._gdiplus_CLASS_GraphicsPathIterator_NextMarker_path_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_NextMarker_path_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\graphicspathiteratornextmarkermethods\nextmarker.htm
ms.date: 12/05/2018
ms.keywords: GraphicsPathIterator class [GDI+],NextMarker method, GraphicsPathIterator.NextMarker, GraphicsPathIterator.NextMarker(GraphicsPath*), GraphicsPathIterator.NextMarker(OUT const GraphicsPath), GraphicsPathIterator::NextMarker, GraphicsPathIterator::NextMarker(OUT const GraphicsPath), NextMarker, NextMarker method [GDI+], NextMarker method [GDI+],GraphicsPathIterator class, _gdiplus_CLASS_GraphicsPathIterator_NextMarker_path_, gdiplus._gdiplus_CLASS_GraphicsPathIterator_NextMarker_path_
req.header: gdipluspath.h
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
 - GraphicsPathIterator::NextMarker
 - gdipluspath/GraphicsPathIterator::NextMarker
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
 - GraphicsPathIterator.NextMarker
---

# GraphicsPathIterator::NextMarker(OUT const GraphicsPath)


## -description

The <b>GraphicsPathIterator::NextMarker</b> method gets the next marker-delimited section of this iterator's associated path.

## -parameters

### -param path [out]

Type: <b><a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object. This method sets the data points of this <b>GraphicsPath</b> object to match the data points of the retrieved section.

## -returns

Type: <b>INT</b>

This method returns the number of data points in the retrieved section. If there are no more marker-delimited sections to retrieve, this method returns 0.

## -remarks

A path has an array of data points that define its lines and curves. You can call a path's <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-setmarker">SetMarker</a> method to designate certain points in the array as markers. Those marker points divide the path into sections.

The first time you call the <b>GraphicsPathIterator::NextMarker</b> method of an iterator, it gets the first marker-delimited section of that iterator's associated path. The second time, it gets the second section, and so on. Each time you call <a href="/previous-versions/ms535462(v=vs.85)">GraphicsPathIterator::NextSubpath</a>, it returns the number of data points in the retrieved section. When there are no sections remaining, it returns 0.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object and adds five figures to the path. The calls to the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-setmarker">SetMarker</a> method place two markers in the path. The first marker is at the end of a figure, and the second marker is in the middle of a figure. The code passes the address of the <b>GraphicsPath</b> object to a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a> constructor to create an iterator that is associated with the path. Then the code calls the iterator's <b>GraphicsPathIterator::NextMarker</b> method twice to obtain the second marker-delimited section of the path. Finally, the code draws the retrieved section of the path.


```cpp

VOID NextMarkerExample(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a graphics path with five figures (subpaths).
   GraphicsPath path;

   path.AddRectangle(Rect(20, 20, 60, 30));
   path.SetMarker();                          // first marker

   path.AddLine(100, 20, 160, 50);
   path.AddArc(180, 20, 60, 30, 0.0f, 180.0f);

   path.AddRectangle(Rect(260, 20, 60, 30));

   path.AddLine(340, 20, 400, 50);
   path.SetMarker();                          // second marker
   path.AddArc(340, 20, 60, 30, 0.0f, 180.0f);
   path.CloseFigure();
  
   path.AddRectangle(Rect(420, 20, 60, 30));
 
   // Create an iterator, and associate it with the path.
   GraphicsPathIterator iterator(&path);

   // Get the second marker-delimited section by calling NextMarker twice.
   GraphicsPath section;
   INT count;
   count = iterator.NextMarker(&section);
   count = iterator.NextMarker(&section);

   // The variable "count" now holds the number of 
   // data points in the second marker-delimited section.

   // Draw the retrieved section.
   Pen bluePen(Color(255, 0, 0, 255));
   graphics.DrawPath(&bluePen, &section);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathdata">GetPathData</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextsubpath(outconstgraphicspath_outbool)">GraphicsPathIterator::NextSubpath Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextmarker(outconstgraphicspath)">NextMarker</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>