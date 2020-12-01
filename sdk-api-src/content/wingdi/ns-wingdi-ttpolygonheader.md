---
UID: NS:wingdi.tagTTPOLYGONHEADER
title: TTPOLYGONHEADER (wingdi.h)
description: The TTPOLYGONHEADER structure specifies the starting position and type of a contour in a TrueType character outline.
helpviewer_keywords: ["*LPTTPOLYGONHEADER","LPTTPOLYGONHEADER","LPTTPOLYGONHEADER structure pointer [Windows GDI]","TTPOLYGONHEADER","TTPOLYGONHEADER structure [Windows GDI]","_win32_TTPOLYGONHEADER_str","gdi.ttpolygonheader","wingdi/LPTTPOLYGONHEADER","wingdi/TTPOLYGONHEADER"]
old-location: gdi\ttpolygonheader.htm
tech.root: gdi
ms.assetid: eea54aeb-7847-4393-87fa-86de93017be8
ms.date: 12/05/2018
ms.keywords: '*LPTTPOLYGONHEADER, LPTTPOLYGONHEADER, LPTTPOLYGONHEADER structure pointer [Windows GDI], TTPOLYGONHEADER, TTPOLYGONHEADER structure [Windows GDI], _win32_TTPOLYGONHEADER_str, gdi.ttpolygonheader, wingdi/LPTTPOLYGONHEADER, wingdi/TTPOLYGONHEADER'
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
req.typenames: TTPOLYGONHEADER, *LPTTPOLYGONHEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTTPOLYGONHEADER
 - wingdi/tagTTPOLYGONHEADER
 - LPTTPOLYGONHEADER
 - wingdi/LPTTPOLYGONHEADER
 - TTPOLYGONHEADER
 - wingdi/TTPOLYGONHEADER
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
 - TTPOLYGONHEADER
---

# TTPOLYGONHEADER structure


## -description

The <b>TTPOLYGONHEADER</b> structure specifies the starting position and type of a contour in a TrueType character outline.

## -struct-fields

### -field cb

The number of bytes required by the <b>TTPOLYGONHEADER</b> structure and <a href="/windows/desktop/api/wingdi/ns-wingdi-ttpolycurve">TTPOLYCURVE</a> structure or structures required to describe the contour of the character.

### -field dwType

The type of character outline returned. Currently, this value must be TT_POLYGON_TYPE.

### -field pfxStart

The starting point of the contour in the character outline.

## -remarks

Each <b>TTPOLYGONHEADER</b> structure is followed by one or more <a href="/windows/desktop/api/wingdi/ns-wingdi-ttpolycurve">TTPOLYCURVE</a> structures.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-pointfx">POINTFX</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-ttpolycurve">TTPOLYCURVE</a>