---
UID: NF:gdipluspath.GraphicsPathIterator.CopyData
title: GraphicsPathIterator::CopyData (gdipluspath.h)
description: The GraphicsPathIterator::CopyData method copies a subset of the path's data points to a PointF array and copies a subset of the path's point types to a BYTE array.
helpviewer_keywords: ["CopyData","CopyData method [GDI+]","CopyData method [GDI+]","GraphicsPathIterator class","GraphicsPathIterator class [GDI+]","CopyData method","GraphicsPathIterator.CopyData","GraphicsPathIterator::CopyData","_gdiplus_CLASS_GraphicsPathIterator_CopyData_points_types_startIndex_endIndex_","gdiplus._gdiplus_CLASS_GraphicsPathIterator_CopyData_points_types_startIndex_endIndex_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_CopyData_points_types_startIndex_endIndex_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\copydata.htm
ms.date: 12/05/2018
ms.keywords: CopyData, CopyData method [GDI+], CopyData method [GDI+],GraphicsPathIterator class, GraphicsPathIterator class [GDI+],CopyData method, GraphicsPathIterator.CopyData, GraphicsPathIterator::CopyData, _gdiplus_CLASS_GraphicsPathIterator_CopyData_points_types_startIndex_endIndex_, gdiplus._gdiplus_CLASS_GraphicsPathIterator_CopyData_points_types_startIndex_endIndex_
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
 - GraphicsPathIterator::CopyData
 - gdipluspath/GraphicsPathIterator::CopyData
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
 - GraphicsPathIterator.CopyData
---

# GraphicsPathIterator::CopyData


## -description

The <b>GraphicsPathIterator::CopyData</b> method copies a subset of the path's data points to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> array and copies a subset of the path's point types to a <b>BYTE</b> array.

## -parameters

### -param points [out]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>*</b>

Pointer to an array that receives a subset of the path's data points.

### -param types [out]

Type: <b>BYTE*</b>

Pointer to an array that receives a subset of the path's point types.

### -param startIndex [in]

Type: <b>INT</b>

Integer that specifies the starting index of the points and types to be copied.

### -param endIndex [in]

Type: <b>INT</b>

Integer that specifies the ending index of the points and types to be copied.

## -returns

Type: <b>INT</b>

This method returns the number of points copied. This is the same as the number of types copied.

## -remarks

This <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a> object is associated with a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object. That <b>GraphicsPath</b> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a> enumeration.

You can call the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-getcount">GraphicsPathIterator::GetCount</a> method to determine the number of data points in the path.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object and adds three lines to the path. The code creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a>&gt; object and calls its <b>GraphicsPathIterator::CopyData</b> method to retrieve the path's points and point types. Then the code displays the count returned by the <b>GraphicsPathIterator::CopyData</b> method.


```cpp

#define BUFFER_SIZE 30
TCHAR numPointsCopied[BUFFER_SIZE];

// Create the points for three lines in a path.
Point pts[] = { Point(20, 20), 
                Point(100, 20), 
                Point(100, 50), 
                Point(20, 50) };
GraphicsPath path;
path.AddLines(pts, 4); // Add the lines to the path.

// Create a GraphicsPathIterator object and associate it with the path. 
GraphicsPathIterator pathIterator(&path);

// Create destination arrays, and copy the path data to them.
PointF* pCopiedPoints = new PointF[4]; 
BYTE* pTypes = new BYTE[4];
INT count = pathIterator.CopyData(pCopiedPoints, pTypes, 0, 3);

// Confirm that the points copied.
StringCchPrintf(
   numPointsCopied, BUFFER_SIZE, TEXT("%d points were copied."), count);

MessageBox(hWnd, numPointsCopied, TEXT("CopyData"), NULL);

delete[] pCopiedPoints;
delete[] pTypes;

```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathdata">GetPathData</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)">GetPathPoints Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathtypes">GetPathTypes</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpointcount">GetPointCount</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-enumerate">GraphicsPathIterator::Enumerate</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-getcount">GraphicsPathIterator::GetCount</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>