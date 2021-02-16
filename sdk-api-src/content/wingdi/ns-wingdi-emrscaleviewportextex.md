---
UID: NS:wingdi.tagEMRSCALEVIEWPORTEXTEX
title: EMRSCALEVIEWPORTEXTEX (wingdi.h)
description: The EMRSCALEVIEWPORTEXTEX and EMRSCALEWINDOWEXTEX structures contain members for the ScaleViewportExtEx and ScaleWindowExtEx enhanced metafile records.
helpviewer_keywords: ["*PEMRSCALEVIEWPORTEXTEX","*PEMRSCALEWINDOWEXTEX","EMRSCALEVIEWPORTEXTEX","EMRSCALEVIEWPORTEXTEX structure [Windows GDI]","EMRSCALEVIEWPORTEXTEX","EMRSCALEWINDOWEXTEX","EMRSCALEVIEWPORTEXTEX","EMRSCALEWINDOWEXTEX structure [Windows GDI]","EMRSCALEWINDOWEXTEX","EMRSCALEWINDOWEXTEX structure [Windows GDI]","PEMRSCALEVIEWPORTEXTEX","PEMRSCALEVIEWPORTEXTEX structure pointer [Windows GDI]","PEMRSCALEWINDOWEXTEX","PEMRSCALEWINDOWEXTEX structure pointer [Windows GDI]","_win32_EMRSCALEVIEWPORTEXTEX_str","gdi.emrscaleviewportextex__emrscalewindowextex","wingdi/EMRSCALEVIEWPORTEXTEX","EMRSCALEWINDOWEXTEX","wingdi/EMRSCALEWINDOWEXTEX","wingdi/PEMRSCALEVIEWPORTEXTEX","wingdi/PEMRSCALEWINDOWEXTEX"]
old-location: gdi\emrscaleviewportextex__emrscalewindowextex.htm
tech.root: gdi
ms.assetid: 712e8b00-d9ab-4b23-aed4-d7aadd0cb3e1
ms.date: 12/05/2018
ms.keywords: '*PEMRSCALEVIEWPORTEXTEX, *PEMRSCALEWINDOWEXTEX, EMRSCALEVIEWPORTEXTEX, EMRSCALEVIEWPORTEXTEX structure [Windows GDI], EMRSCALEVIEWPORTEXTEX,EMRSCALEWINDOWEXTEX, EMRSCALEVIEWPORTEXTEX,EMRSCALEWINDOWEXTEX structure [Windows GDI], EMRSCALEWINDOWEXTEX, EMRSCALEWINDOWEXTEX structure [Windows GDI], PEMRSCALEVIEWPORTEXTEX, PEMRSCALEVIEWPORTEXTEX structure pointer [Windows GDI], PEMRSCALEWINDOWEXTEX, PEMRSCALEWINDOWEXTEX structure pointer [Windows GDI], _win32_EMRSCALEVIEWPORTEXTEX_str, gdi.emrscaleviewportextex__emrscalewindowextex, wingdi/EMRSCALEVIEWPORTEXTEX,EMRSCALEWINDOWEXTEX, wingdi/EMRSCALEWINDOWEXTEX, wingdi/PEMRSCALEVIEWPORTEXTEX, wingdi/PEMRSCALEWINDOWEXTEX'
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
req.typenames: EMRSCALEVIEWPORTEXTEX, *PEMRSCALEVIEWPORTEXTEX, EMRSCALEWINDOWEXTEX, *PEMRSCALEWINDOWEXTEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRSCALEVIEWPORTEXTEX
 - wingdi/tagEMRSCALEVIEWPORTEXTEX
 - PEMRSCALEVIEWPORTEXTEX
 - wingdi/PEMRSCALEVIEWPORTEXTEX
 - EMRSCALEVIEWPORTEXTEX
 - wingdi/EMRSCALEVIEWPORTEXTEX
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
 - EMRSCALEVIEWPORTEXTEX
---

# EMRSCALEVIEWPORTEXTEX structure


## -description

The <b>EMRSCALEVIEWPORTEXTEX</b> and <b>EMRSCALEWINDOWEXTEX</b> structures contain members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-scaleviewportextex">ScaleViewportExtEx</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-scalewindowextex">ScaleWindowExtEx</a> enhanced metafile records.

## -struct-fields

### -field emr

Base structure for all record types.

### -field xNum

Horizontal multiplicand.

### -field xDenom

Horizontal divisor.

### -field yNum

Vertical multiplicand.

### -field yDenom

Vertical divisor.

## -see-also

<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>