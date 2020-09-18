---
UID: NS:wingdi.tagEMRSELECTPALETTE
title: EMRSELECTPALETTE (wingdi.h)
description: The EMRSELECTPALETTE structure contains members for the SelectPalette enhanced metafile record. Note that the bForceBackground parameter in SelectPalette is always recorded as TRUE, which causes the palette to be realized as a background palette.
helpviewer_keywords: ["*PEMRSELECTPALETTE","EMRSELECTPALETTE","EMRSELECTPALETTE structure [Windows GDI]","PEMRSELECTPALETTE","PEMRSELECTPALETTE structure pointer [Windows GDI]","_win32_EMRSELECTPALETTE_str","gdi.emrselectpalette","wingdi/EMRSELECTPALETTE","wingdi/PEMRSELECTPALETTE"]
old-location: gdi\emrselectpalette.htm
tech.root: gdi
ms.assetid: f83367c0-406a-4a5f-961f-8e5afe6707fd
ms.date: 12/05/2018
ms.keywords: '*PEMRSELECTPALETTE, EMRSELECTPALETTE, EMRSELECTPALETTE structure [Windows GDI], PEMRSELECTPALETTE, PEMRSELECTPALETTE structure pointer [Windows GDI], _win32_EMRSELECTPALETTE_str, gdi.emrselectpalette, wingdi/EMRSELECTPALETTE, wingdi/PEMRSELECTPALETTE'
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
req.typenames: EMRSELECTPALETTE, *PEMRSELECTPALETTE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRSELECTPALETTE
 - wingdi/tagEMRSELECTPALETTE
 - PEMRSELECTPALETTE
 - wingdi/PEMRSELECTPALETTE
 - EMRSELECTPALETTE
 - wingdi/EMRSELECTPALETTE
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
 - EMRSELECTPALETTE
---

# EMRSELECTPALETTE structure


## -description

The <b>EMRSELECTPALETTE</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-selectpalette">SelectPalette</a> enhanced metafile record. Note that the <i>bForceBackground</i> parameter in <b>SelectPalette</b> is always recorded as <b>TRUE</b>, which causes the palette to be realized as a background palette.

## -struct-fields

### -field emr

The base structure for all record types.

### -field ihPal

Index to logical palette in the handle table.

## -see-also

<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectpalette">SelectPalette</a>