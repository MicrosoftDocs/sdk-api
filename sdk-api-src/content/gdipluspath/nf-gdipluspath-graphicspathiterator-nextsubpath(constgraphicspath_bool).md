---
UID: NF:gdipluspath.GraphicsPathIterator.NextSubpath(constGraphicsPath,BOOL)
title: GraphicsPathIterator::NextSubpath(OUT const GraphicsPath,OUT BOOL) (gdipluspath.h)
description: The GraphicsPathIterator::NextSubpath method gets the next figure (subpath) from this iterator's associated path.
helpviewer_keywords: ["GraphicsPathIterator class [GDI+]","NextSubpath method","GraphicsPathIterator.NextSubpath","GraphicsPathIterator.NextSubpath(GraphicsPath*","BOOL*)","GraphicsPathIterator.NextSubpath(OUT const GraphicsPath","OUT BOOL)","GraphicsPathIterator::NextSubpath","GraphicsPathIterator::NextSubpath(OUT const GraphicsPath","OUT BOOL)","NextSubpath","NextSubpath method [GDI+]","NextSubpath method [GDI+]","GraphicsPathIterator class","_gdiplus_CLASS_GraphicsPathIterator_NextSubpath_path_isClosed_","gdiplus._gdiplus_CLASS_GraphicsPathIterator_NextSubpath_path_isClosed_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_NextSubpath_path_isClosed_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\graphicspathiteratornextsubpathmethods\nextsubpath.htm
ms.date: 12/05/2018
ms.keywords: GraphicsPathIterator class [GDI+],NextSubpath method, GraphicsPathIterator.NextSubpath, GraphicsPathIterator.NextSubpath(GraphicsPath*,BOOL*), GraphicsPathIterator.NextSubpath(OUT const GraphicsPath,OUT BOOL), GraphicsPathIterator::NextSubpath, GraphicsPathIterator::NextSubpath(OUT const GraphicsPath,OUT BOOL), NextSubpath, NextSubpath method [GDI+], NextSubpath method [GDI+],GraphicsPathIterator class, _gdiplus_CLASS_GraphicsPathIterator_NextSubpath_path_isClosed_, gdiplus._gdiplus_CLASS_GraphicsPathIterator_NextSubpath_path_isClosed_
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
 - GraphicsPathIterator::NextSubpath
 - gdipluspath/GraphicsPathIterator::NextSubpath
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
 - GraphicsPathIterator.NextSubpath
---

# GraphicsPathIterator::NextSubpath(OUT const GraphicsPath,OUT BOOL)


## -description

The <b>GraphicsPathIterator::NextSubpath</b> method gets the next figure (subpath) from this iterator's associated path.

## -parameters

### -param path [out]

Type: <b><a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object. This method sets the data points of this <b>GraphicsPath</b> object to match the data points of the retrieved figure.

### -param isClosed [out]

Type: <b>BOOL*</b>

Pointer to a <b>BOOL</b> that receives a value that indicates whether the retrieved figure is closed. If the figure is closed, the received value is <b>TRUE</b>; otherwise, the received value is <b>FALSE</b>.

## -returns

Type: <b>INT</b>

This method returns the number of data points in the retrieved figure. If there are no more figures to retrieve, this method returns 0.

## -remarks

The first time you call the <b>GraphicsPathIterator::NextSubpath</b> method of an iterator, it gets the first figure (subpath) of that iterator's associated path. The second time, it gets the second figure, and so on. Each time you call <b>GraphicsPathIterator::NextSubpath</b>, it returns the number of data points in the retrieved figure. When there are no figures remaining, it returns 0.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object and adds five figures (also called subpaths) to the path. The code passes the address of the <b>GraphicsPath</b> object to a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a> constructor to create an iterator that is associated with the path. The code calls the iterator's <b>GraphicsPathIterator::NextSubpath</b> method twice to retrieve the second figure (subpath) from the path. Then the code calls the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath">DrawPath</a> method of a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object to draw that individual subpath.


```cpp

VOID NextSubpathExample(HDC hdc)
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

   // Get the second subpath by calling NextSubpath twice.
   GraphicsPath subpath;
   BOOL isClosed;
   INT count;
   count = iterator.NextSubpath(&subpath, &isClosed);
   count = iterator.NextSubpath(&subpath, &isClosed);

   // The variable "count" now holds the number of 
   // data points in the second subpath.

   // Draw the retrieved subpath.
   Pen bluePen(Color(255, 0, 0, 255));
   graphics.DrawPath(&bluePen, &subpath);
}

```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathdata">GetPathData</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-getsubpathcount">GraphicsPathIterator::GetSubpathCount</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextmarker(outconstgraphicspath)">GraphicsPathIterator::NextMarker Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextsubpath(outconstgraphicspath_outbool)">NextSubpath</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>