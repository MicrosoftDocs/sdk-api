---
UID: NS:wingdi.tagEMRINVERTRGN
title: EMRINVERTRGN (wingdi.h)
description: The EMRINVERTRGN and EMRPAINTRGN structures contain members for the InvertRgn and PaintRgn enhanced metafile records.
helpviewer_keywords: ["*PEMRINVERTRGN","*PEMRPAINTRGN","EMRINVERTRGN","EMRINVERTRGN structure [Windows GDI]","EMRINVERTRGN","EMRPAINTRGN","EMRINVERTRGN","EMRPAINTRGN structure [Windows GDI]","EMRPAINTRGN","EMRPAINTRGN structure [Windows GDI]","PEMRINVERTRGN","PEMRINVERTRGN structure pointer [Windows GDI]","PEMRPAINTRGN","PEMRPAINTRGN structure pointer [Windows GDI]","_win32_EMRINVERTRGN_str","gdi.emrinvertrgn__emrpaintrgn","wingdi/EMRINVERTRGN","EMRPAINTRGN","wingdi/EMRPAINTRGN","wingdi/PEMRINVERTRGN","wingdi/PEMRPAINTRGN"]
old-location: gdi\emrinvertrgn__emrpaintrgn.htm
tech.root: gdi
ms.assetid: 91c0badc-bd26-418a-9cdb-3e70e7337021
ms.date: 12/05/2018
ms.keywords: '*PEMRINVERTRGN, *PEMRPAINTRGN, EMRINVERTRGN, EMRINVERTRGN structure [Windows GDI], EMRINVERTRGN,EMRPAINTRGN, EMRINVERTRGN,EMRPAINTRGN structure [Windows GDI], EMRPAINTRGN, EMRPAINTRGN structure [Windows GDI], PEMRINVERTRGN, PEMRINVERTRGN structure pointer [Windows GDI], PEMRPAINTRGN, PEMRPAINTRGN structure pointer [Windows GDI], _win32_EMRINVERTRGN_str, gdi.emrinvertrgn__emrpaintrgn, wingdi/EMRINVERTRGN,EMRPAINTRGN, wingdi/EMRPAINTRGN, wingdi/PEMRINVERTRGN, wingdi/PEMRPAINTRGN'
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
req.typenames: EMRINVERTRGN, *PEMRINVERTRGN, EMRPAINTRGN, *PEMRPAINTRGN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRINVERTRGN
 - wingdi/tagEMRINVERTRGN
 - PEMRINVERTRGN
 - wingdi/PEMRINVERTRGN
 - EMRINVERTRGN
 - wingdi/EMRINVERTRGN
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
 - EMRINVERTRGN
---

# EMRINVERTRGN structure


## -description

The <b>EMRINVERTRGN</b> and <b>EMRPAINTRGN</b> structures 
		  contain members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-invertrgn">InvertRgn</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-paintrgn">PaintRgn</a> enhanced metafile records.

## -struct-fields

### -field emr

Base structure for all record types.

### -field rclBounds

Bounding rectangle, in device units.

### -field cbRgnData

Size of region data, in bytes.

### -field RgnData

Buffer containing an <a href="/windows/desktop/api/wingdi/ns-wingdi-rgndata">RGNDATA</a> structure.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-invertrgn">InvertRgn</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-paintrgn">PaintRgn</a>