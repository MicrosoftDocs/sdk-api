---
UID: NS:wingdi.tagEMRSETPALETTEENTRIES
title: EMRSETPALETTEENTRIES (wingdi.h)
description: The EMRSETPALETTEENTRIES structure contains members for the SetPaletteEntries enhanced metafile record.
helpviewer_keywords: ["*PEMRSETPALETTEENTRIES","EMRSETPALETTEENTRIES","EMRSETPALETTEENTRIES structure [Windows GDI]","PEMRSETPALETTEENTRIES","PEMRSETPALETTEENTRIES structure pointer [Windows GDI]","_win32_EMRSETPALETTEENTRIES_str","gdi.emrsetpaletteentries","wingdi/EMRSETPALETTEENTRIES","wingdi/PEMRSETPALETTEENTRIES"]
old-location: gdi\emrsetpaletteentries.htm
tech.root: gdi
ms.assetid: df75567e-150f-4f88-b6ae-938b451a7b7d
ms.date: 12/05/2018
ms.keywords: '*PEMRSETPALETTEENTRIES, EMRSETPALETTEENTRIES, EMRSETPALETTEENTRIES structure [Windows GDI], PEMRSETPALETTEENTRIES, PEMRSETPALETTEENTRIES structure pointer [Windows GDI], _win32_EMRSETPALETTEENTRIES_str, gdi.emrsetpaletteentries, wingdi/EMRSETPALETTEENTRIES, wingdi/PEMRSETPALETTEENTRIES'
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
req.typenames: EMRSETPALETTEENTRIES, *PEMRSETPALETTEENTRIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRSETPALETTEENTRIES
 - wingdi/tagEMRSETPALETTEENTRIES
 - PEMRSETPALETTEENTRIES
 - wingdi/PEMRSETPALETTEENTRIES
 - EMRSETPALETTEENTRIES
 - wingdi/EMRSETPALETTEENTRIES
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
 - EMRSETPALETTEENTRIES
---

# EMRSETPALETTEENTRIES structure


## -description

The <b>EMRSETPALETTEENTRIES</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-setpaletteentries">SetPaletteEntries</a> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field ihPal

Palette handle index.

### -field iStart

Index of first entry to set.

### -field cEntries

Number of entries.

### -field aPalEntries

Array of <a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a> structures. Note that <b>peFlags</b> members in the structures do not contain any flags.

## -see-also

<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setpaletteentries">SetPaletteEntries</a>