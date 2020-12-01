---
UID: NS:wingdi.tagEMREOF
title: EMREOF (wingdi.h)
description: The EMREOF structure contains data for the enhanced metafile record that indicates the end of the metafile.
helpviewer_keywords: ["*PEMREOF","EMREOF","EMREOF structure [Windows GDI]","PEMREOF","PEMREOF structure pointer [Windows GDI]","_win32_EMREOF_str","gdi.emreof","wingdi/EMREOF","wingdi/PEMREOF"]
old-location: gdi\emreof.htm
tech.root: gdi
ms.assetid: 99a3f97e-cb43-49b3-9972-23f9911b2cd0
ms.date: 12/05/2018
ms.keywords: '*PEMREOF, EMREOF, EMREOF structure [Windows GDI], PEMREOF, PEMREOF structure pointer [Windows GDI], _win32_EMREOF_str, gdi.emreof, wingdi/EMREOF, wingdi/PEMREOF'
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
req.typenames: EMREOF, *PEMREOF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMREOF
 - wingdi/tagEMREOF
 - PEMREOF
 - wingdi/PEMREOF
 - EMREOF
 - wingdi/EMREOF
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
 - EMREOF
---

# EMREOF structure


## -description

The <b>EMREOF</b> structure contains data for the enhanced metafile record that indicates the end of the metafile.

## -struct-fields

### -field emr

The base structure for all record types.

### -field nPalEntries

The number of palette entries.

### -field offPalEntries

The offset, in bytes, to an array of <a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a> structures.

### -field nSizeLast

The same size as the <b>nSize</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-emr">EMR</a> structure. This member must be the last double word of the record. If palette entries exist, they precede this member.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-emr">EMR</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a>