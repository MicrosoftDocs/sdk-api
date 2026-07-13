---
UID: NF:gdipluspath.GraphicsPath.StartFigure
title: GraphicsPath::StartFigure (gdipluspath.h)
description: The GraphicsPath::StartFigure method starts a new figure without closing the current figure. Subsequent points added to this path are added to the new figure.
helpviewer_keywords: ["GraphicsPath class [GDI+]","StartFigure method","GraphicsPath.StartFigure","GraphicsPath::StartFigure","StartFigure","StartFigure method [GDI+]","StartFigure method [GDI+]","GraphicsPath class","_gdiplus_CLASS_GraphicsPath_StartFigure_","gdiplus._gdiplus_CLASS_GraphicsPath_StartFigure_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_StartFigure_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\startfigure.htm
ms.date: 12/05/2018
ms.keywords: GraphicsPath class [GDI+],StartFigure method, GraphicsPath.StartFigure, GraphicsPath::StartFigure, StartFigure, StartFigure method [GDI+], StartFigure method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_StartFigure_, gdiplus._gdiplus_CLASS_GraphicsPath_StartFigure_
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
 - GraphicsPath::StartFigure
 - gdipluspath/GraphicsPath::StartFigure
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
 - GraphicsPath.StartFigure
---

# GraphicsPath::StartFigure


## -description

The <b>GraphicsPath::StartFigure</b> method starts a new figure without closing the current figure. Subsequent points added to this path are added to the new figure.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-closefigure">GraphicsPath::CloseFigure</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextsubpath(outconstgraphicspath_outbool)">GraphicsPathIterator::NextSubpath Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>
