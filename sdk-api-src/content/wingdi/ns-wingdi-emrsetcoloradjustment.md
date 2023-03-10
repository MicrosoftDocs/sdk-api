---
UID: NS:wingdi.tagEMRSETCOLORADJUSTMENT
title: EMRSETCOLORADJUSTMENT (wingdi.h)
description: The EMRSETCOLORADJUSTMENT structure contains members for the SetColorAdjustment enhanced metafile record.
helpviewer_keywords: ["*PEMRSETCOLORADJUSTMENT","EMRSETCOLORADJUSTMENT","EMRSETCOLORADJUSTMENT structure [Windows GDI]","PEMRSETCOLORADJUSTMENT","PEMRSETCOLORADJUSTMENT structure pointer [Windows GDI]","_win32_EMRSETCOLORADJUSTMENT_str","gdi.emrsetcoloradjustment","wingdi/EMRSETCOLORADJUSTMENT","wingdi/PEMRSETCOLORADJUSTMENT"]
old-location: gdi\emrsetcoloradjustment.htm
tech.root: gdi
ms.assetid: d9f99f71-d102-484f-beb4-0d2de1070345
ms.date: 12/05/2018
ms.keywords: '*PEMRSETCOLORADJUSTMENT, EMRSETCOLORADJUSTMENT, EMRSETCOLORADJUSTMENT structure [Windows GDI], PEMRSETCOLORADJUSTMENT, PEMRSETCOLORADJUSTMENT structure pointer [Windows GDI], _win32_EMRSETCOLORADJUSTMENT_str, gdi.emrsetcoloradjustment, wingdi/EMRSETCOLORADJUSTMENT, wingdi/PEMRSETCOLORADJUSTMENT'
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
req.typenames: EMRSETCOLORADJUSTMENT, *PEMRSETCOLORADJUSTMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRSETCOLORADJUSTMENT
 - wingdi/tagEMRSETCOLORADJUSTMENT
 - PEMRSETCOLORADJUSTMENT
 - wingdi/PEMRSETCOLORADJUSTMENT
 - EMRSETCOLORADJUSTMENT
 - wingdi/EMRSETCOLORADJUSTMENT
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
 - EMRSETCOLORADJUSTMENT
---

# EMRSETCOLORADJUSTMENT structure


## -description

The <b>EMRSETCOLORADJUSTMENT</b> structure contains members for the <b>SetColorAdjustment</b> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field ColorAdjustment

A <a href="/windows/desktop/api/wingdi/ns-wingdi-coloradjustment">COLORADJUSTMENT</a> structure.

## -see-also

<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setcoloradjustment">SetColorAdjustment</a>