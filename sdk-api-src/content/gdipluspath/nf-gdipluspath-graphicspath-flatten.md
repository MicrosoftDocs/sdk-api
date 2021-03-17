---
UID: NF:gdipluspath.GraphicsPath.Flatten
title: GraphicsPath::Flatten (gdipluspath.h)
description: The GraphicsPath::Flatten method applies a transformation to this path and converts each curve in the path to a sequence of connected lines.
helpviewer_keywords: ["Flatten","Flatten method [GDI+]","Flatten method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","Flatten method","GraphicsPath.Flatten","GraphicsPath::Flatten","_gdiplus_CLASS_GraphicsPath_Flatten_matrix_flatness_","gdiplus._gdiplus_CLASS_GraphicsPath_Flatten_matrix_flatness_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_Flatten_matrix_flatness_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\flatten.htm
ms.date: 12/05/2018
ms.keywords: Flatten, Flatten method [GDI+], Flatten method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],Flatten method, GraphicsPath.Flatten, GraphicsPath::Flatten, _gdiplus_CLASS_GraphicsPath_Flatten_matrix_flatness_, gdiplus._gdiplus_CLASS_GraphicsPath_Flatten_matrix_flatness_
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
 - GraphicsPath::Flatten
 - gdipluspath/GraphicsPath::Flatten
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
 - GraphicsPath.Flatten
---

# GraphicsPath::Flatten


## -description

The <b>GraphicsPath::Flatten</b> method applies a transformation to this path and converts each curve in the path to a sequence of connected lines.

## -parameters

### -param matrix [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Optional. Pointer to a <a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that specifies the transformation to be applied to the path's data points. The default value is <b>NULL</b>, which specifies that no transformation is to be applied.

### -param flatness [in]

Type: <b>REAL</b>

Optional. Real number that specifies the maximum error between the path and its flattened approximation. Reducing the flatness increases the number of line segments in the approximation. The default value is <code>FlatnessDefault</code>, which is a constant defined in Gdiplusenums.h.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-flattening-paths-about">Flattening Paths</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>