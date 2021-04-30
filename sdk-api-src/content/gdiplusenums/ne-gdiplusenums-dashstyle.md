---
UID: NE:gdiplusenums.DashStyle
title: DashStyle (gdiplusenums.h)
description: The DashStyle enumeration specifies the line style of a line drawn with a Windows GDI+ pen. The line can be drawn by using one of several predefined styles or a custom style.
helpviewer_keywords: ["DashStyle","DashStyle enumeration [GDI+]","DashStyleCustom","DashStyleDash","DashStyleDashDot","DashStyleDashDotDot","DashStyleDot","DashStyleSolid","_gdiplus_ENUM_DashStyle","gdiplus._gdiplus_ENUM_DashStyle","gdiplusenums/DashStyle","gdiplusenums/DashStyleCustom","gdiplusenums/DashStyleDash","gdiplusenums/DashStyleDashDot","gdiplusenums/DashStyleDashDotDot","gdiplusenums/DashStyleDot","gdiplusenums/DashStyleSolid"]
old-location: gdiplus\_gdiplus_ENUM_DashStyle.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\dashstyle.htm
ms.date: 12/05/2018
ms.keywords: DashStyle, DashStyle enumeration [GDI+], DashStyleCustom, DashStyleDash, DashStyleDashDot, DashStyleDashDotDot, DashStyleDot, DashStyleSolid, _gdiplus_ENUM_DashStyle, gdiplus._gdiplus_ENUM_DashStyle, gdiplusenums/DashStyle, gdiplusenums/DashStyleCustom, gdiplusenums/DashStyleDash, gdiplusenums/DashStyleDashDot, gdiplusenums/DashStyleDashDotDot, gdiplusenums/DashStyleDot, gdiplusenums/DashStyleSolid
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
 - DashStyle
 - gdiplusenums/DashStyle
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
 - DashStyle
---

# DashStyle enumeration


## -description

The <b>DashStyle</b> enumeration specifies the line style of a line drawn with a Windows GDI+ pen. The line can be drawn by using one of several predefined styles or a custom style.

## -enum-fields

### -field DashStyleSolid

Specifies a solid line.

### -field DashStyleDash

Specifies a dashed line.

### -field DashStyleDot

Specifies a dotted line.

### -field DashStyleDashDot

Specifies an alternating dash-dot line.

### -field DashStyleDashDotDot

Specifies an alternating dash-dot-dot line.

### -field DashStyleCustom

Specifies a user-defined, custom dashed line.

## -remarks

A custom dashed line is created by calling the 
				<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setdashpattern">Pen::SetDashPattern</a> method, which takes an array of values for the dash lengths and the space lengths.