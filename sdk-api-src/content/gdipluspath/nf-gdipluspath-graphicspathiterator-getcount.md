---
UID: NF:gdipluspath.GraphicsPathIterator.GetCount
title: GraphicsPathIterator::GetCount (gdipluspath.h)
description: The GraphicsPathIterator::GetCount method returns the number of data points in the path.
helpviewer_keywords: ["GetCount","GetCount method [GDI+]","GetCount method [GDI+]","GraphicsPathIterator class","GraphicsPathIterator class [GDI+]","GetCount method","GraphicsPathIterator.GetCount","GraphicsPathIterator::GetCount","_gdiplus_CLASS_GraphicsPathIterator_GetCount_","gdiplus._gdiplus_CLASS_GraphicsPathIterator_GetCount_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_GetCount_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\getcount.htm
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [GDI+], GetCount method [GDI+],GraphicsPathIterator class, GraphicsPathIterator class [GDI+],GetCount method, GraphicsPathIterator.GetCount, GraphicsPathIterator::GetCount, _gdiplus_CLASS_GraphicsPathIterator_GetCount_, gdiplus._gdiplus_CLASS_GraphicsPathIterator_GetCount_
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
 - GraphicsPathIterator::GetCount
 - gdipluspath/GraphicsPathIterator::GetCount
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
 - GraphicsPathIterator.GetCount
---

# GraphicsPathIterator::GetCount


## -description

The <b>GraphicsPathIterator::GetCount</b> method returns the number of data points in the path.



## -returns

Type: <b>INT</b>

This method returns the number of data points in the path.

## -remarks

This <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a> object is associated with a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object. That <b>GraphicsPath</b> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a> enumeration.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object and then adds a rectangle and an ellipse to the path. The code passes the address of that <b>GraphicsPath</b> object to a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a> constructor to create an iterator that is associated with the path. The code calls the iterator's <b>GraphicsPathIterator::GetCount</b> method to determine the number of data points in the path. The call to <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-enumerate">GraphicsPathIterator::Enumerate</a> retrieves two arrays from the path: one that holds the path's data points and one that holds the path's point types. After the data points have been retrieved, the code calls the <a href="/previous-versions/ms535967(v=vs.85)">FillEllipse</a> method of a  object to draw each of the data points.


```cpp

VOID GetCountExample(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path that has a rectangle and an ellipse.
   GraphicsPath path;
   path.AddRectangle(Rect(20, 20, 60, 30));
   path.AddEllipse(Rect(20, 70, 100, 50));

   // Create an iterator, and associate it with the path.
   GraphicsPathIterator iterator(&path);

   // Get the number of data points in the path.
   INT count = iterator.GetCount();

   // Get the data points.
   PointF* points = new PointF[count];
   BYTE* types = new BYTE[count];
   iterator.Enumerate(points, types, count);

   // Draw the data points.
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



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathdata">GetPathData</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)">GetPathPoints Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathtypes">GetPathTypes</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpointcount">GetPointCount</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-copydata">GraphicsPathIterator::CopyData</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-enumerate">GraphicsPathIterator::Enumerate</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>
