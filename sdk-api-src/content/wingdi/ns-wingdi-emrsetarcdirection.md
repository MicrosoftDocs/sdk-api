---
UID: NS:wingdi.tagEMRSETARCDIRECTION
title: EMRSETARCDIRECTION (wingdi.h)
description: The EMRSETARCDIRECTION structure contains members for the SetArcDirection enhanced metafile record.
helpviewer_keywords: ["*PEMRSETARCDIRECTION","EMRSETARCDIRECTION","EMRSETARCDIRECTION structure [Windows GDI]","PEMRSETARCDIRECTION","PEMRSETARCDIRECTION structure pointer [Windows GDI]","_win32_EMRSETARCDIRECTION_str","gdi.emrsetarcdirection","wingdi/EMRSETARCDIRECTION","wingdi/PEMRSETARCDIRECTION"]
old-location: gdi\emrsetarcdirection.htm
tech.root: gdi
ms.assetid: d33d329f-7f66-4995-b80f-656c96ea105b
ms.date: 12/05/2018
ms.keywords: '*PEMRSETARCDIRECTION, EMRSETARCDIRECTION, EMRSETARCDIRECTION structure [Windows GDI], PEMRSETARCDIRECTION, PEMRSETARCDIRECTION structure pointer [Windows GDI], _win32_EMRSETARCDIRECTION_str, gdi.emrsetarcdirection, wingdi/EMRSETARCDIRECTION, wingdi/PEMRSETARCDIRECTION'
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
req.typenames: EMRSETARCDIRECTION, *PEMRSETARCDIRECTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRSETARCDIRECTION
 - wingdi/tagEMRSETARCDIRECTION
 - PEMRSETARCDIRECTION
 - wingdi/PEMRSETARCDIRECTION
 - EMRSETARCDIRECTION
 - wingdi/EMRSETARCDIRECTION
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
 - EMRSETARCDIRECTION
---

# EMRSETARCDIRECTION structure


## -description

The <b>EMRSETARCDIRECTION</b> structure contains members for the <b>SetArcDirection</b> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field iArcDirection

Arc direction. This member can be either the AD_CLOCKWISE or AD_COUNTERCLOCKWISE value.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-arc">Arc</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setarcdirection">SetArcDirection</a>