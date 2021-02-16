---
UID: NF:gdipluspath.GraphicsPath.GetPathTypes
title: GraphicsPath::GetPathTypes (gdipluspath.h)
description: The GraphicsPath::GetPathTypes method gets this path's array of point types.
helpviewer_keywords: ["GetPathTypes","GetPathTypes method [GDI+]","GetPathTypes method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","GetPathTypes method","GraphicsPath.GetPathTypes","GraphicsPath::GetPathTypes","_gdiplus_CLASS_GraphicsPath_GetPathTypes_types_count_","gdiplus._gdiplus_CLASS_GraphicsPath_GetPathTypes_types_count_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GetPathTypes_types_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\getpathtypes.htm
ms.date: 12/05/2018
ms.keywords: GetPathTypes, GetPathTypes method [GDI+], GetPathTypes method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],GetPathTypes method, GraphicsPath.GetPathTypes, GraphicsPath::GetPathTypes, _gdiplus_CLASS_GraphicsPath_GetPathTypes_types_count_, gdiplus._gdiplus_CLASS_GraphicsPath_GetPathTypes_types_count_
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
 - GraphicsPath::GetPathTypes
 - gdipluspath/GraphicsPath::GetPathTypes
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
 - GraphicsPath.GetPathTypes
---

# GraphicsPath::GetPathTypes


## -description

The <b>GraphicsPath::GetPathTypes</b> method gets this path's array of point types.

## -parameters

### -param types [out]

Type: <b>BYTE*</b>

Pointer to an array that receives the point types. You must allocate memory for this array. You can call the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpointcount">GraphicsPath::GetPointCount</a> method to determine the required size of the array.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>types</i> array. Set this parameter equal to the return value of the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpointcount">GraphicsPath::GetPointCount</a> method.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a> enumeration.


#### Examples



The following example creates a path and adds a sequence of three connected lines to the path. The code calls the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpointcount">GraphicsPath::GetPointCount</a> method to determine the number of bytes in the path's array of point types and then allocates a buffer large enough to hold that array. Then the code calls the <b>GraphicsPath::GetPathTypes</b> method to fill the buffer with the array of point types.


```cpp
GraphicsPath path;
Point pts[] = {Point(0, 0), Point(2, 2), Point(3, 3), Point(0, 5)};
path.AddLines(pts, 4);
INT num = path.GetPointCount();
BYTE* pTypes = new BYTE[num];
path.GetPathTypes(pTypes, num);
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)">GetPathPoints Methods</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathdata">GraphicsPath::GetPathData</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpointcount">GraphicsPath::GetPointCount</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pathdata">PathData</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>