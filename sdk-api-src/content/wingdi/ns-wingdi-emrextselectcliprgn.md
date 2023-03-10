---
UID: NS:wingdi.tagEMREXTSELECTCLIPRGN
title: EMREXTSELECTCLIPRGN (wingdi.h)
description: The EMREXTSELECTCLIPRGN structure contains members for the ExtSelectClipRgn enhanced metafile record.
helpviewer_keywords: ["*PEMREXTSELECTCLIPRGN","EMREXTSELECTCLIPRGN","EMREXTSELECTCLIPRGN structure [Windows GDI]","PEMREXTSELECTCLIPRGN","PEMREXTSELECTCLIPRGN structure pointer [Windows GDI]","_win32_EMREXTSELECTCLIPRGN_str","gdi.emrextselectcliprgn","wingdi/EMREXTSELECTCLIPRGN","wingdi/PEMREXTSELECTCLIPRGN"]
old-location: gdi\emrextselectcliprgn.htm
tech.root: gdi
ms.assetid: fcfa0ae1-06e0-4313-9140-496aa4eec9da
ms.date: 12/05/2018
ms.keywords: '*PEMREXTSELECTCLIPRGN, EMREXTSELECTCLIPRGN, EMREXTSELECTCLIPRGN structure [Windows GDI], PEMREXTSELECTCLIPRGN, PEMREXTSELECTCLIPRGN structure pointer [Windows GDI], _win32_EMREXTSELECTCLIPRGN_str, gdi.emrextselectcliprgn, wingdi/EMREXTSELECTCLIPRGN, wingdi/PEMREXTSELECTCLIPRGN'
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
req.typenames: EMREXTSELECTCLIPRGN, *PEMREXTSELECTCLIPRGN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMREXTSELECTCLIPRGN
 - wingdi/tagEMREXTSELECTCLIPRGN
 - PEMREXTSELECTCLIPRGN
 - wingdi/PEMREXTSELECTCLIPRGN
 - EMREXTSELECTCLIPRGN
 - wingdi/EMREXTSELECTCLIPRGN
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
 - EMREXTSELECTCLIPRGN
---

# EMREXTSELECTCLIPRGN structure


## -description

The <b>EMREXTSELECTCLIPRGN</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-extselectcliprgn">ExtSelectClipRgn</a> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field cbRgnData

Size of region data, in bytes.

### -field iMode

Operation to be performed. This member must be one of the following values: RGN_AND, RGN_COPY, RGN_DIFF, RGN_OR, or RGN_XOR.

### -field RgnData

Buffer containing a <a href="/windows/desktop/api/wingdi/ns-wingdi-rgndata">RGNDATA</a> structure.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-extselectcliprgn">ExtSelectClipRgn</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>