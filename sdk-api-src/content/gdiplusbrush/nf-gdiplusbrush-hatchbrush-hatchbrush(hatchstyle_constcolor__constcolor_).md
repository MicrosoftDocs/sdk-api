---
UID: NF:gdiplusbrush.HatchBrush.HatchBrush(HatchStyle,constColor&,constColor&)
title: HatchBrush::HatchBrush(IN HatchStyle,IN const Color &,IN const Color &) (gdiplusbrush.h)
description: Creates a HatchBrush::HatchBrush object based on a hatch style, a foreground color, and a background color.
helpviewer_keywords: ["HatchBrush","HatchBrush class [GDI+]","HatchBrush constructor","HatchBrush constructor [GDI+]","HatchBrush constructor [GDI+]","HatchBrush class","HatchBrush.HatchBrush","HatchBrush.HatchBrush(IN HatchStyle","IN const Color &","IN const Color &)","HatchBrush::HatchBrush","HatchBrush::HatchBrush(IN HatchStyle","IN const Color &","IN const Color &)","_gdiplus_CLASS_HatchBrush_HatchBrush_hatchStyle_foreColor_backColor_","gdiplus._gdiplus_CLASS_HatchBrush_HatchBrush_hatchStyle_foreColor_backColor_"]
old-location: gdiplus\_gdiplus_CLASS_HatchBrush_HatchBrush_hatchStyle_foreColor_backColor_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\hatchbrushclass\hatchbrush_47hatchstyle_forecolor_backcolor.htm
ms.date: 12/05/2018
ms.keywords: HatchBrush, HatchBrush class [GDI+],HatchBrush constructor, HatchBrush constructor [GDI+], HatchBrush constructor [GDI+],HatchBrush class, HatchBrush.HatchBrush, HatchBrush.HatchBrush(IN HatchStyle,IN const Color &,IN const Color &), HatchBrush::HatchBrush, HatchBrush::HatchBrush(IN HatchStyle,IN const Color &,IN const Color &), _gdiplus_CLASS_HatchBrush_HatchBrush_hatchStyle_foreColor_backColor_, gdiplus._gdiplus_CLASS_HatchBrush_HatchBrush_hatchStyle_foreColor_backColor_
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
 - HatchBrush::HatchBrush
 - gdiplusbrush/HatchBrush::HatchBrush
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
 - HatchBrush.HatchBrush
---

## -description

Creates a <b>HatchBrush::HatchBrush</b> object based on a hatch style, a foreground color, and a background color.

## -parameters

### -param hatchStyle [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-hatchstyle">HatchStyle</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-hatchstyle">HatchStyle</a> enumeration that specifies the pattern of hatch lines that will be used.

### -param foreColor [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Reference to a color to use for the hatch lines.

### -param backColor [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Optional. Reference to a color to use for the background. The default value is <b>Color</b>()(a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object created by the default <b>Color</b> constructor).

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush">HatchBrush</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-hatchstyle">HatchStyle</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-brush-to-fill-shapes-use">Using a Brush to Fill Shapes</a>