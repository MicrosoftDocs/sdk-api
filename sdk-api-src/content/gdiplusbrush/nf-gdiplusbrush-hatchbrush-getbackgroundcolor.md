---
UID: NF:gdiplusbrush.HatchBrush.GetBackgroundColor
title: HatchBrush::GetBackgroundColor (gdiplusbrush.h)
description: The HatchBrush::GetBackgroundColor method gets the background color of this hatch brush.
helpviewer_keywords: ["GetBackgroundColor","GetBackgroundColor method [GDI+]","GetBackgroundColor method [GDI+]","HatchBrush class","HatchBrush class [GDI+]","GetBackgroundColor method","HatchBrush.GetBackgroundColor","HatchBrush::GetBackgroundColor","_gdiplus_CLASS_HatchBrush_GetBackgroundColor_color_","gdiplus._gdiplus_CLASS_HatchBrush_GetBackgroundColor_color_"]
old-location: gdiplus\_gdiplus_CLASS_HatchBrush_GetBackgroundColor_color_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\hatchbrushclass\hatchbrushmethods\getbackgroundcolor.htm
ms.date: 12/05/2018
ms.keywords: GetBackgroundColor, GetBackgroundColor method [GDI+], GetBackgroundColor method [GDI+],HatchBrush class, HatchBrush class [GDI+],GetBackgroundColor method, HatchBrush.GetBackgroundColor, HatchBrush::GetBackgroundColor, _gdiplus_CLASS_HatchBrush_GetBackgroundColor_color_, gdiplus._gdiplus_CLASS_HatchBrush_GetBackgroundColor_color_
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
 - HatchBrush::GetBackgroundColor
 - gdiplusbrush/HatchBrush::GetBackgroundColor
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
 - HatchBrush.GetBackgroundColor
---

# HatchBrush::GetBackgroundColor


## -description

The <b>HatchBrush::GetBackgroundColor</b> method gets the background color of this hatch brush.

## -parameters

### -param color [out]

Type: <b><a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that receives the background color. The background color defines the color over which the hatch lines are drawn.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-hatch-pattern-use">Filling a Shape with a Hatch Pattern</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush">HatchBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-hatchbrush-getforegroundcolor">HatchBrush::GetForegroundColor</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-hatchstyle">HatchStyle</a>