---
UID: NF:gdipluspath.GraphicsPath.Transform
title: GraphicsPath::Transform (gdipluspath.h)
description: The GraphicsPath::Transform method multiplies each of this path's data points by a specified matrix.
helpviewer_keywords: ["GraphicsPath class [GDI+]","Transform method","GraphicsPath.Transform","GraphicsPath::Transform","Transform","Transform method [GDI+]","Transform method [GDI+]","GraphicsPath class","_gdiplus_CLASS_GraphicsPath_Transform_matrix_","gdiplus._gdiplus_CLASS_GraphicsPath_Transform_matrix_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_Transform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\transform.htm
ms.date: 12/05/2018
ms.keywords: GraphicsPath class [GDI+],Transform method, GraphicsPath.Transform, GraphicsPath::Transform, Transform, Transform method [GDI+], Transform method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_Transform_matrix_, gdiplus._gdiplus_CLASS_GraphicsPath_Transform_matrix_
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
 - GraphicsPath::Transform
 - gdipluspath/GraphicsPath::Transform
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
 - GraphicsPath.Transform
---

# GraphicsPath::Transform


## -description

The <b>GraphicsPath::Transform</b> method multiplies each of this path's data points by a specified matrix.

## -parameters

### -param matrix [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that specifies the transformation.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-matrix-representation-of-transformations-about">Matrix Representation of Transformations</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>