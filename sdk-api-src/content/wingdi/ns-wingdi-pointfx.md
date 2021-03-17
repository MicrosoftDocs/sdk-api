---
UID: NS:wingdi.tagPOINTFX
title: POINTFX (wingdi.h)
description: The POINTFX structure contains the coordinates of points that describe the outline of a character in a TrueType font.
helpviewer_keywords: ["*LPPOINTFX","LPPOINTFX","LPPOINTFX structure pointer [Windows GDI]","POINTFX","POINTFX structure [Windows GDI]","_win32_POINTFX_str","gdi.pointfx","wingdi/LPPOINTFX","wingdi/POINTFX"]
old-location: gdi\pointfx.htm
tech.root: gdi
ms.assetid: a8736c6c-7944-42ed-811c-308f41f1ab2f
ms.date: 12/05/2018
ms.keywords: '*LPPOINTFX, LPPOINTFX, LPPOINTFX structure pointer [Windows GDI], POINTFX, POINTFX structure [Windows GDI], _win32_POINTFX_str, gdi.pointfx, wingdi/LPPOINTFX, wingdi/POINTFX'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: POINTFX, *LPPOINTFX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPOINTFX
 - wingdi/tagPOINTFX
 - LPPOINTFX
 - wingdi/LPPOINTFX
 - POINTFX
 - wingdi/POINTFX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - POINTFX
---

# POINTFX structure


## -description

The <b>POINTFX</b> structure contains the coordinates of points that describe the outline of a character in a TrueType font.

## -struct-fields

### -field x

The x-component of a point on the outline of a TrueType character.

### -field y

The y-component of a point on the outline of a TrueType character.

## -remarks

The <b>POINTFX</b> structure is a member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-ttpolycurve">TTPOLYCURVE</a> and <a href="/windows/desktop/api/wingdi/ns-wingdi-ttpolygonheader">TTPOLYGONHEADER</a> structures. Values in the <b>POINTFX</b> structure are specified in device units.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-fixed">FIXED</a>



<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-ttpolycurve">TTPOLYCURVE</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-ttpolygonheader">TTPOLYGONHEADER</a>