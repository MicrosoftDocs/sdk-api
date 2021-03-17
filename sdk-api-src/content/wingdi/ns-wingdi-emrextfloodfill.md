---
UID: NS:wingdi.tagEMREXTFLOODFILL
title: EMREXTFLOODFILL (wingdi.h)
description: The EMREXTFLOODFILL structure contains members for the ExtFloodFill enhanced metafile record.
helpviewer_keywords: ["*PEMREXTFLOODFILL","EMREXTFLOODFILL","EMREXTFLOODFILL structure [Windows GDI]","PEMREXTFLOODFILL","PEMREXTFLOODFILL structure pointer [Windows GDI]","_win32_EMREXTFLOODFILL_str","gdi.emrextfloodfill","wingdi/EMREXTFLOODFILL","wingdi/PEMREXTFLOODFILL"]
old-location: gdi\emrextfloodfill.htm
tech.root: gdi
ms.assetid: 93c80ea4-42f3-4c0a-8f72-76d2a6634e15
ms.date: 12/05/2018
ms.keywords: '*PEMREXTFLOODFILL, EMREXTFLOODFILL, EMREXTFLOODFILL structure [Windows GDI], PEMREXTFLOODFILL, PEMREXTFLOODFILL structure pointer [Windows GDI], _win32_EMREXTFLOODFILL_str, gdi.emrextfloodfill, wingdi/EMREXTFLOODFILL, wingdi/PEMREXTFLOODFILL'
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
req.typenames: EMREXTFLOODFILL, *PEMREXTFLOODFILL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMREXTFLOODFILL
 - wingdi/tagEMREXTFLOODFILL
 - PEMREXTFLOODFILL
 - wingdi/PEMREXTFLOODFILL
 - EMREXTFLOODFILL
 - wingdi/EMREXTFLOODFILL
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
 - EMREXTFLOODFILL
---

# EMREXTFLOODFILL structure


## -description

The <b>EMREXTFLOODFILL</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-extfloodfill">ExtFloodFill</a> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field ptlStart

Coordinates, in logical units, where filling begins.

### -field crColor

Color of fill. To make a <a href="/windows/desktop/gdi/colorref">COLORREF</a> value, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

### -field iMode

Type of fill operation to be performed. This member must be either the FLOODFILLBORDER or FLOODFILLSURFACE value.

## -see-also

<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-extfloodfill">ExtFloodFill</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>