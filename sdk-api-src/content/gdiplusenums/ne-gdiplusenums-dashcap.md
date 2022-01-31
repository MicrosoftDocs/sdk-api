---
UID: NE:gdiplusenums.DashCap
title: DashCap (gdiplusenums.h)
description: The DashCap enumeration specifies the type of graphic shape to use on both ends of each dash in a dashed line.
helpviewer_keywords: ["DashCap","DashCap enumeration [GDI+]","DashCapFlat","DashCapRound","DashCapTriangle","_gdiplus_ENUM_DashCap","gdiplus._gdiplus_ENUM_DashCap","gdiplusenums/DashCap","gdiplusenums/DashCapFlat","gdiplusenums/DashCapRound","gdiplusenums/DashCapTriangle"]
old-location: gdiplus\_gdiplus_ENUM_DashCap.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\dashcap.htm
ms.date: 12/05/2018
ms.keywords: DashCap, DashCap enumeration [GDI+], DashCapFlat, DashCapRound, DashCapTriangle, _gdiplus_ENUM_DashCap, gdiplus._gdiplus_ENUM_DashCap, gdiplusenums/DashCap, gdiplusenums/DashCapFlat, gdiplusenums/DashCapRound, gdiplusenums/DashCapTriangle
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
 - DashCap
 - gdiplusenums/DashCap
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
 - DashCap
---

# DashCap enumeration


## -description

The <b>DashCap</b> enumeration specifies the type of graphic shape to use on both ends of each dash in a dashed line.

## -enum-fields

### -field DashCapFlat:0

Specifies a square cap that squares off both ends of each dash.

### -field DashCapRound:2

Specifies a circular cap that rounds off both ends of each dash.

### -field DashCapTriangle:3

Specifies a triangular cap that points both ends of each dash.

## -remarks

If you set the alignment of a 
				<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object to <b>PenAlignmentInset</b>, you cannot use that pen to draw triangular dash caps.
