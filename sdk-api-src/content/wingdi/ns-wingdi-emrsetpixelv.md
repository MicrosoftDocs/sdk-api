---
UID: NS:wingdi.tagEMRSETPIXELV
title: EMRSETPIXELV (wingdi.h)
description: The EMRSETPIXELV structure contains members for the SetPixelV enhanced metafile record. When an enhanced metafile is created, calls to SetPixel are also recorded in this record.
helpviewer_keywords: ["*PEMRSETPIXELV","EMRSETPIXELV","EMRSETPIXELV structure [Windows GDI]","PEMRSETPIXELV","PEMRSETPIXELV structure pointer [Windows GDI]","_win32_EMRSETPIXELV_str","gdi.emrsetpixelv","wingdi/EMRSETPIXELV","wingdi/PEMRSETPIXELV"]
old-location: gdi\emrsetpixelv.htm
tech.root: gdi
ms.assetid: 1487d788-c85a-4a58-a4c8-8abe198944b4
ms.date: 12/05/2018
ms.keywords: '*PEMRSETPIXELV, EMRSETPIXELV, EMRSETPIXELV structure [Windows GDI], PEMRSETPIXELV, PEMRSETPIXELV structure pointer [Windows GDI], _win32_EMRSETPIXELV_str, gdi.emrsetpixelv, wingdi/EMRSETPIXELV, wingdi/PEMRSETPIXELV'
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
req.typenames: EMRSETPIXELV, *PEMRSETPIXELV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRSETPIXELV
 - wingdi/tagEMRSETPIXELV
 - PEMRSETPIXELV
 - wingdi/PEMRSETPIXELV
 - EMRSETPIXELV
 - wingdi/EMRSETPIXELV
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
 - EMRSETPIXELV
---

# EMRSETPIXELV structure


## -description

The <b>EMRSETPIXELV</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-setpixelv">SetPixelV</a> enhanced metafile record. When an enhanced metafile is created, calls to <a href="/windows/desktop/api/wingdi/nf-wingdi-setpixel">SetPixel</a> are also recorded in this record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field ptlPixel

Logical coordinates of pixel.

### -field crColor

Color value. To make a <a href="/windows/desktop/gdi/colorref">COLORREF</a> value, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

## -see-also

<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setpixel">SetPixel</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setpixelv">SetPixelV</a>