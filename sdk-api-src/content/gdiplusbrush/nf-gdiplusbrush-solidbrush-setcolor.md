---
UID: NF:gdiplusbrush.SolidBrush.SetColor
title: SolidBrush::SetColor (gdiplusbrush.h)
description: The SolidBrush::SetColor method sets the color of this solid brush.
helpviewer_keywords: ["SetColor","SetColor method [GDI+]","SetColor method [GDI+]","SolidBrush class","SolidBrush class [GDI+]","SetColor method","SolidBrush.SetColor","SolidBrush::SetColor","_gdiplus_CLASS_SolidBrush_SetColor_color_","gdiplus._gdiplus_CLASS_SolidBrush_SetColor_color_"]
old-location: gdiplus\_gdiplus_CLASS_SolidBrush_SetColor_color_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\solidbrushclass\solidbrushmethods\setcolor_9color.htm
ms.date: 12/05/2018
ms.keywords: SetColor, SetColor method [GDI+], SetColor method [GDI+],SolidBrush class, SolidBrush class [GDI+],SetColor method, SolidBrush.SetColor, SolidBrush::SetColor, _gdiplus_CLASS_SolidBrush_SetColor_color_, gdiplus._gdiplus_CLASS_SolidBrush_SetColor_color_
req.header: gdiplusbrush.h
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
 - SolidBrush::SetColor
 - gdiplusbrush/SolidBrush::SetColor
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
 - SolidBrush.SetColor
---

# SolidBrush::SetColor


## -description

The <b>SolidBrush::SetColor</b> method sets the color of this solid brush.

## -parameters

### -param color [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Reference to a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the color to be set in this solid brush.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-solid-color-use">Filling a Shape with a Solid Color</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor">SolidBrush::GetColor</a>