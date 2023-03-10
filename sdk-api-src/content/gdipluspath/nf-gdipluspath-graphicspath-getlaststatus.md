---
UID: NF:gdipluspath.GraphicsPath.GetLastStatus
title: GraphicsPath::GetLastStatus (gdipluspath.h)
description: The GraphicsPath::GetLastStatus method returns a value that indicates the nature of this GraphicsPath object's most recent method failure.
helpviewer_keywords: ["GetLastStatus","GetLastStatus method [GDI+]","GetLastStatus method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","GetLastStatus method","GraphicsPath.GetLastStatus","GraphicsPath::GetLastStatus","_gdiplus_CLASS_GraphicsPath_GetLastStatus_","gdiplus._gdiplus_CLASS_GraphicsPath_GetLastStatus_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GetLastStatus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\getlaststatus_91.htm
ms.date: 12/05/2018
ms.keywords: GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],GetLastStatus method, GraphicsPath.GetLastStatus, GraphicsPath::GetLastStatus, _gdiplus_CLASS_GraphicsPath_GetLastStatus_, gdiplus._gdiplus_CLASS_GraphicsPath_GetLastStatus_
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
 - GraphicsPath::GetLastStatus
 - gdipluspath/GraphicsPath::GetLastStatus
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
 - GraphicsPath.GetLastStatus
---

# GraphicsPath::GetLastStatus


## -description

The <b>GraphicsPath::GetLastStatus</b> method returns a value that indicates the nature of this <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object's most recent method failure.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

The <b>GraphicsPath::GetLastStatus</b> method returns an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If no methods invoked on this <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object have failed since the previous call to <b>GraphicsPath::GetLastStatus</b>, then <b>GraphicsPath::GetLastStatus</b> returns Ok.

If at least one method invoked on this <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object has failed since the previous call to <b>GraphicsPath::GetLastStatus</b>, then <b>GraphicsPath::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.

## -remarks

You can call <b>GraphicsPath::GetLastStatus</b> immediately after constructing a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object to determine whether the constructor succeeded.

The first time you call the <b>GraphicsPath::GetLastStatus</b> method of a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object, it returns Ok if the constructor succeeded and all methods invoked so far on the <b>GraphicsPath</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
