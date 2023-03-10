---
UID: NF:gdiplusgraphics.Graphics.DrawPath
title: Graphics::DrawPath (gdiplusgraphics.h)
description: The Graphics::DrawPath method draws a sequence of lines and curves defined by a GraphicsPath object.
helpviewer_keywords: ["DrawPath","DrawPath method [GDI+]","DrawPath method [GDI+]","Graphics class","Graphics class [GDI+]","DrawPath method","Graphics.DrawPath","Graphics::DrawPath","_gdiplus_CLASS_Graphics_DrawPath_pen_path_","gdiplus._gdiplus_CLASS_Graphics_DrawPath_pen_path_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawPath_pen_path_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\drawpath.htm
ms.date: 12/05/2018
ms.keywords: DrawPath, DrawPath method [GDI+], DrawPath method [GDI+],Graphics class, Graphics class [GDI+],DrawPath method, Graphics.DrawPath, Graphics::DrawPath, _gdiplus_CLASS_Graphics_DrawPath_pen_path_, gdiplus._gdiplus_CLASS_Graphics_DrawPath_pen_path_
req.header: gdiplusgraphics.h
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
 - Graphics::DrawPath
 - gdiplusgraphics/Graphics::DrawPath
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
 - Graphics.DrawPath
---

# Graphics::DrawPath


## -description

The <b>Graphics::DrawPath</b> method draws a sequence of lines and curves defined by a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object.

## -parameters

### -param pen [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>*</b>

Pointer to a pen that is used to draw the path.

### -param path [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object that specifies the sequence of lines and curves that make up the path.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-creating-figures-from-lines-curves-and-shapes-use">Creating Figures from Lines, Curves, and Shapes</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inconstrect__inreal_inreal)">FillPie Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>