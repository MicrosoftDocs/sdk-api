---
UID: NS:wingdi.tagEMRFILLRGN
title: EMRFILLRGN (wingdi.h)
description: The EMRFILLRGN structure contains members for the FillRgn enhanced metafile record.
old-location: gdi\emrfillrgn.htm
tech.root: gdi
ms.assetid: 84b81b9d-3def-403c-94cd-8f5ddea02d6d
ms.date: 12/05/2018
ms.keywords: '*PEMRFILLRGN, EMRFILLRGN, EMRFILLRGN structure [Windows GDI], PEMRFILLRGN, PEMRFILLRGN structure pointer [Windows GDI], _win32_EMRFILLRGN_str, gdi.emrfillrgn, wingdi/EMRFILLRGN, wingdi/PEMRFILLRGN'
f1_keywords:
- wingdi/EMRFILLRGN
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wingdi.h
api_name:
- EMRFILLRGN
targetos: Windows
req.typenames: EMRFILLRGN, *PEMRFILLRGN
req.redist: 
ms.custom: 19H1
---

# EMRFILLRGN structure


## -description



The <b>EMRFILLRGN</b> structure contains members for the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-fillrgn">FillRgn</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field rclBounds

Bounding rectangle, in device units.


### -field cbRgnData

Size of region data, in bytes.


### -field ihBrush

Index of brush, in handle table.


### -field RgnData

Buffer containing <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-rgndata">RGNDATA</a> structure.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-fillrgn">FillRgn</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-rgndata">RGNDATA</a>
 

 

