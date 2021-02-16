---
UID: NF:gdipluspath.GraphicsPath.GraphicsPath(FillMode)
title: GraphicsPath::GraphicsPath(IN FillMode) (gdipluspath.h)
description: Creates a GraphicsPath::GraphicsPath object and initializes the fill mode. This is the default constructor.
helpviewer_keywords: ["GraphicsPath","GraphicsPath class [GDI+]","GraphicsPath constructor","GraphicsPath constructor [GDI+]","GraphicsPath constructor [GDI+]","GraphicsPath class","GraphicsPath.GraphicsPath","GraphicsPath.GraphicsPath(FillMode)","GraphicsPath.GraphicsPath(IN FillMode)","GraphicsPath::GraphicsPath","GraphicsPath::GraphicsPath(IN FillMode)","_gdiplus_CLASS_GraphicsPath_GraphicsPath_fillMode_","gdiplus._gdiplus_CLASS_GraphicsPath_GraphicsPath_fillMode_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GraphicsPath_fillMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathconstructors\graphicspath_97fillmode.htm
ms.date: 12/05/2018
ms.keywords: GraphicsPath, GraphicsPath class [GDI+],GraphicsPath constructor, GraphicsPath constructor [GDI+], GraphicsPath constructor [GDI+],GraphicsPath class, GraphicsPath.GraphicsPath, GraphicsPath.GraphicsPath(FillMode), GraphicsPath.GraphicsPath(IN FillMode), GraphicsPath::GraphicsPath, GraphicsPath::GraphicsPath(IN FillMode), _gdiplus_CLASS_GraphicsPath_GraphicsPath_fillMode_, gdiplus._gdiplus_CLASS_GraphicsPath_GraphicsPath_fillMode_
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
 - GraphicsPath::GraphicsPath
 - gdipluspath/GraphicsPath::GraphicsPath
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
 - GraphicsPath.GraphicsPath
---

# GraphicsPath::GraphicsPath(IN FillMode)


## -description

Creates a <b>GraphicsPath::GraphicsPath</b> object and initializes the fill mode. This is the default constructor.

## -parameters

### -param fillMode [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fillmode">FillMode</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fillmode">FillMode</a> enumeration that specifies how areas are filled if the path intersects itself. The default value is <code>FillModeAlternate</code>.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fillmode">FillMode</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-graphicspath(constgraphicspath_)">GraphicsPath Constructors</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>