---
UID: NF:gdipluspath.GraphicsPathIterator.Enumerate
title: GraphicsPathIterator::Enumerate (gdipluspath.h)
description: The GraphicsPathIterator::Enumerate method copies the path's data points to a PointF array and copies the path's point types to a BYTE array.
helpviewer_keywords: ["Enumerate","Enumerate method [GDI+]","Enumerate method [GDI+]","GraphicsPathIterator class","GraphicsPathIterator class [GDI+]","Enumerate method","GraphicsPathIterator.Enumerate","GraphicsPathIterator::Enumerate","_gdiplus_CLASS_GraphicsPathIterator_Enumerate_points_types_count_","gdiplus._gdiplus_CLASS_GraphicsPathIterator_Enumerate_points_types_count_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_Enumerate_points_types_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\enumerate.htm
ms.date: 12/05/2018
ms.keywords: Enumerate, Enumerate method [GDI+], Enumerate method [GDI+],GraphicsPathIterator class, GraphicsPathIterator class [GDI+],Enumerate method, GraphicsPathIterator.Enumerate, GraphicsPathIterator::Enumerate, _gdiplus_CLASS_GraphicsPathIterator_Enumerate_points_types_count_, gdiplus._gdiplus_CLASS_GraphicsPathIterator_Enumerate_points_types_count_
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
 - GraphicsPathIterator::Enumerate
 - gdipluspath/GraphicsPathIterator::Enumerate
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
 - GraphicsPathIterator.Enumerate
---

# GraphicsPathIterator::Enumerate


## -description

The <b>GraphicsPathIterator::Enumerate</b> method copies the path's data points to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> array and copies the path's point types to a <b>BYTE</b> array.

## -parameters

### -param points [out]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>*</b>

Pointer to an array that receives the path's data points.

### -param types [out]

Type: <b>BYTE*</b>

Pointer to an array that receives the path's point types.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>points</i> array. This is the same as the number of elements in the <i>types</i> array.

## -returns

Type: <b>INT</b>

This method returns the number of points retrieved.

## -remarks

This 
				<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a> object is associated with a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object. That <b>GraphicsPath</b> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a> enumeration.

You can call the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-getcount">GraphicsPathIterator::GetCount</a> method to determine the number of data points in the path. The <i>points</i> parameter points to a buffer that receives the data points, and the <i>types</i> parameter points to a buffer that receives the types. Before you call the <b>GraphicsPathIterator::Enumerate</b> method, you must allocate memory for those buffers. The size of the <i>points</i> buffer should be the return value of <b>GraphicsPathIterator::GetCount</b> multiplied by <b>sizeof(PointF)</b>. The size of the types buffer should be the return value of <b>GraphicsPathIterator::GetCount</b>.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object and adds three lines to the path. The code creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a> object and calls its <b>GraphicsPathIterator::Enumerate</b> method to retrieve the path's data points and point types. Then the code displays the count returned by the <b>GraphicsPathIterator::Enumerate</b> method.


```cpp

#define BUFFER_SIZE 30
TCHAR numPointsEnum[BUFFER_SIZE];

// Add some lines to a path.
Point pts[] = {Point(20, 20), 
                Point(100, 20), 
                Point(100, 50), 
                Point(20, 50)};
GraphicsPath path;
path.AddLines(pts, 4);

// Create a GraphicsPathIterator object, and associate it with the path.
GraphicsPathIterator pathIterator(&path);

// Create destination arrays, and copy the path data to them.
UINT c = pathIterator.GetCount();
PointF* pEnumPoints = new PointF[c]; 
BYTE* pTypes = new BYTE[c];
INT count = pathIterator.Enumerate(pEnumPoints, pTypes, c);

// Confirm that the points were enumerated.
StringCchPrintf(
   numPointsEnum, BUFFER_SIZE, TEXT("%d points were enumerated."), count);

MessageBox(hWnd, numPointsEnum, TEXT("Enumerate"), NULL);

delete[] pEnumPoints;
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



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-copydata">GraphicsPathIterator::CopyData</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-getcount">GraphicsPathIterator::GetCount</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>