---
UID: NE:gdiplusenums.PenType
title: PenType (gdiplusenums.h)
description: The PenType enumeration indicates the type of pattern, texture, or gradient that a pen draws.
helpviewer_keywords: ["PenType","PenType enumeration [GDI+]","PenTypeHatchFill","PenTypeLinearGradient","PenTypePathGradient","PenTypeSolidColor","PenTypeTextureFill","PenTypeUnknown","_gdiplus_ENUM_PenType","gdiplus._gdiplus_ENUM_PenType","gdiplusenums/PenType","gdiplusenums/PenTypeHatchFill","gdiplusenums/PenTypeLinearGradient","gdiplusenums/PenTypePathGradient","gdiplusenums/PenTypeSolidColor","gdiplusenums/PenTypeTextureFill","gdiplusenums/PenTypeUnknown"]
old-location: gdiplus\_gdiplus_ENUM_PenType.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\pentype.htm
ms.date: 12/05/2018
ms.keywords: PenType, PenType enumeration [GDI+], PenTypeHatchFill, PenTypeLinearGradient, PenTypePathGradient, PenTypeSolidColor, PenTypeTextureFill, PenTypeUnknown, _gdiplus_ENUM_PenType, gdiplus._gdiplus_ENUM_PenType, gdiplusenums/PenType, gdiplusenums/PenTypeHatchFill, gdiplusenums/PenTypeLinearGradient, gdiplusenums/PenTypePathGradient, gdiplusenums/PenTypeSolidColor, gdiplusenums/PenTypeTextureFill, gdiplusenums/PenTypeUnknown
req.header: gdiplusenums.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - PenType
 - gdiplusenums/PenType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - PenType
---

# PenType enumeration


## -description

The <b>PenType</b> enumeration indicates the type of pattern, texture, or gradient that a pen draws.

## -enum-fields

### -field PenTypeSolidColor

Indicates that the pen draws with a solid color.

### -field PenTypeHatchFill

Indicates that the pen draws with a hatch pattern that is specified by a 
				<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush">HatchBrush</a> object.

### -field PenTypeTextureFill

Indicates that the pen draws with a texture that is specified by a 
				<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush">TextureBrush</a> object.

### -field PenTypePathGradient

Indicates that the pen draws with a color gradient that is specified by a 
				<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object.

### -field PenTypeLinearGradient

Indicates that the pen draws with a color gradient that is specified by a 
				<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a> object.

### -field PenTypeUnknown:-1

Indicates that the pen type is unknown.

## -remarks

A pen's type is determined when the pen is constructed. For example, if you pass a 
				<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush">HatchBrush</a> object to a 
				<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> constructor, then the pen that is constructed has a pen type of <b><b>PenTypeHatchFill</b></b>. If you pass a 
				<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object or a 
				<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a> object to a 
				<b>Pen</b> constructor, then the pen that is constructed has a pen type of <b><b>PenTypeSolidColor</b></b>.
