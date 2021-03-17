---
UID: NS:wingdi.tagEMRRESIZEPALETTE
title: EMRRESIZEPALETTE (wingdi.h)
description: The EMRRESIZEPALETTE structure contains members for the ResizePalette enhanced metafile record.
helpviewer_keywords: ["*PEMRRESIZEPALETTE","EMRRESIZEPALETTE","EMRRESIZEPALETTE structure [Windows GDI]","PEMRRESIZEPALETTE","PEMRRESIZEPALETTE structure pointer [Windows GDI]","_win32_EMRRESIZEPALETTE_str","gdi.emrresizepalette","wingdi/EMRRESIZEPALETTE","wingdi/PEMRRESIZEPALETTE"]
old-location: gdi\emrresizepalette.htm
tech.root: gdi
ms.assetid: b9c31591-bf9f-44d9-8c9a-9682d29fc541
ms.date: 12/05/2018
ms.keywords: '*PEMRRESIZEPALETTE, EMRRESIZEPALETTE, EMRRESIZEPALETTE structure [Windows GDI], PEMRRESIZEPALETTE, PEMRRESIZEPALETTE structure pointer [Windows GDI], _win32_EMRRESIZEPALETTE_str, gdi.emrresizepalette, wingdi/EMRRESIZEPALETTE, wingdi/PEMRRESIZEPALETTE'
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
req.typenames: EMRRESIZEPALETTE, *PEMRRESIZEPALETTE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRRESIZEPALETTE
 - wingdi/tagEMRRESIZEPALETTE
 - PEMRRESIZEPALETTE
 - wingdi/PEMRRESIZEPALETTE
 - EMRRESIZEPALETTE
 - wingdi/EMRRESIZEPALETTE
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
 - EMRRESIZEPALETTE
---

# EMRRESIZEPALETTE structure


## -description

The <b>EMRRESIZEPALETTE</b> structure contains members for the <b>ResizePalette</b> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field ihPal

Index of the palette in the handle table.

### -field cEntries

Number of entries in palette after resizing.

## -see-also

<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-resizepalette">ResizePalette</a>