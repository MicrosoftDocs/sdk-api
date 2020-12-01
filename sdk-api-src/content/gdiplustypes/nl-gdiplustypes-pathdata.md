---
UID: NL:gdiplustypes.PathData
title: PathData (gdiplustypes.h)
description: The PathData class is a helper class for the GraphicsPath and GraphicsPathIterator classes.
helpviewer_keywords: ["PathData","PathData class [GDI+]","PathData class [GDI+]","described","_gdiplus_CLASS_PathData_Class","gdiplus._gdiplus_CLASS_PathData_Class","gdiplustypes/PathData"]
old-location: gdiplus\_gdiplus_CLASS_PathData_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathdata.htm
ms.date: 12/05/2018
ms.keywords: PathData, PathData class [GDI+], PathData class [GDI+],described, _gdiplus_CLASS_PathData_Class, gdiplus._gdiplus_CLASS_PathData_Class, gdiplustypes/PathData
req.header: gdiplustypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PathData
 - gdiplustypes/PathData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdiplustypes.h
api_name:
 - PathData
---

## -description

The <b>PathData</b> class is a helper class for the <a href="/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> and <a href="/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a> classes. A <b>GraphicsPath</b> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. You can use a <b>PathData</b> object to get or set the data points (and their types) of a path.

## -see-also

<a href="/windows/win32/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and drawing paths</a>

<a href="/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)">GetPathPoints methods</a>

<a href="/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathdata">GraphicsPath::GetPathData</a>

<a href="/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathtypes">GraphicsPath::GetPathTypes</a>

<a href="/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpointcount">GraphicsPath::GetPointCount</a>

<a href="/windows/win32/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a>

<a href="/windows/win32/gdiplus/-gdiplus-paths-about">Paths</a>

<a href="/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>

