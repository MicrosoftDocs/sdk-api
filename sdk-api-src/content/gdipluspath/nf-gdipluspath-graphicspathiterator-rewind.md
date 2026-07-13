---
UID: NF:gdipluspath.GraphicsPathIterator.Rewind
title: GraphicsPathIterator::Rewind (gdipluspath.h)
description: The GraphicsPathIterator::Rewind method rewinds this iterator to the beginning of its associated path.
helpviewer_keywords: ["GraphicsPathIterator class [GDI+]","Rewind method","GraphicsPathIterator.Rewind","GraphicsPathIterator::Rewind","Rewind","Rewind method [GDI+]","Rewind method [GDI+]","GraphicsPathIterator class","_gdiplus_CLASS_GraphicsPathIterator_Rewind_","gdiplus._gdiplus_CLASS_GraphicsPathIterator_Rewind_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_Rewind_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\rewind.htm
ms.date: 12/05/2018
ms.keywords: GraphicsPathIterator class [GDI+],Rewind method, GraphicsPathIterator.Rewind, GraphicsPathIterator::Rewind, Rewind, Rewind method [GDI+], Rewind method [GDI+],GraphicsPathIterator class, _gdiplus_CLASS_GraphicsPathIterator_Rewind_, gdiplus._gdiplus_CLASS_GraphicsPathIterator_Rewind_
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
 - GraphicsPathIterator::Rewind
 - gdipluspath/GraphicsPathIterator::Rewind
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - api-ms-win-crt-stdio-l1-1-0.dll
 - Gdiplus.dll
api_name:
 - GraphicsPathIterator.Rewind
---

# GraphicsPathIterator::Rewind


## -description

The <b>GraphicsPathIterator::Rewind</b> method rewinds this iterator to the beginning of its associated path.



## -remarks

The first time you call the 
				<b>NextSubpath</b> method of an iterator, it gets the first figure (subpath) of that iterator's associated path. The second time, it gets the second figure, and so on. When you call <b>GraphicsPathIterator::Rewind</b>, the sequence starts over; that is, after you call <b>GraphicsPathIterator::Rewind</b>, the next call to <a href="/previous-versions/ms535462(v=vs.85)">GraphicsPathIterator::NextSubpath</a> gets the first figure in the path. The <a href="/previous-versions/ms535464(v=vs.85)">GraphicsPathIterator::NextMarker</a> and <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextpathtype">GraphicsPathIterator::NextPathType</a> methods behave similarly.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object and adds five figures to the path. The code passes the address of that <b>GraphicsPath</b> object to a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a> constructor to create an iterator that is associated with the path. The code calls the iterator's <a href="/previous-versions/ms535462(v=vs.85)">GraphicsPathIterator::NextSubpath</a> method twice to retrieve the second figure in the path. The <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath">DrawPath</a> method draws that path in blue. Next, the code calls the <b>GraphicsPathIterator::Rewind</b> method and then calls <b>GraphicsPathIterator::NextSubpath</b> once to obtain the first figure in the path. The <b>DrawPath</b> method draws that figure in red.


```cpp

VOID RewindExample(HDC hdc)
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

   // Draw the second figure in blue.
   Pen bluePen(Color(255, 0, 0, 255));
   graphics.DrawPath(&bluePen, &subpath);

   // Rewind the iterator, and get the first figure in the path.
   iterator.Rewind();
   count = iterator.NextSubpath(&subpath, &isClosed);

   // Draw the first figure in red.
   Pen redPen(Color(255, 255, 0, 0));
   graphics.DrawPath(&redPen, &subpath);
}

```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextmarker(outconstgraphicspath)">GraphicsPathIterator::NextMarker Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextpathtype">GraphicsPathIterator::NextPathType</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextsubpath(outconstgraphicspath_outbool)">GraphicsPathIterator::NextSubpath Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>
