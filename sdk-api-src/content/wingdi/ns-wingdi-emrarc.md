---
UID: NS:wingdi.tagEMRARC
title: EMRARC (wingdi.h)
description: The EMRARC, EMRARCTO, EMRCHORD, and EMRPIE structures contain members for the Arc, ArcTo, Chord, and Pie enhanced metafile records.
helpviewer_keywords: ["*PEMRARC","*PEMRARCTO","*PEMRCHORD","*PEMRPIE","EMRARC","EMRARC structure [Windows GDI]","EMRARC","EMRARCTO","EMRCHORD","EMRPIE","EMRARC","EMRARCTO","EMRCHORD","EMRPIE structure [Windows GDI]","EMRARCTO","EMRARCTO structure [Windows GDI]","EMRCHORD","EMRCHORD structure [Windows GDI]","EMRPIE","EMRPIE structure [Windows GDI]","PEMRARC","PEMRARC structure pointer [Windows GDI]","PEMRARCTO","PEMRARCTO structure pointer [Windows GDI]","PEMRCHORD","PEMRCHORD structure pointer [Windows GDI]","PEMRPIE","PEMRPIE structure pointer [Windows GDI]","_win32_EMRARC_str","gdi.emrarc__emrarcto__emrchord__emrpie","wingdi/EMRARC","EMRARCTO","EMRCHORD","EMRPIE","wingdi/EMRARCTO","wingdi/EMRCHORD","wingdi/EMRPIE","wingdi/PEMRARC","wingdi/PEMRARCTO","wingdi/PEMRCHORD","wingdi/PEMRPIE"]
old-location: gdi\emrarc__emrarcto__emrchord__emrpie.htm
tech.root: gdi
ms.assetid: f249b396-bf71-401b-b972-317d551fc9aa
ms.date: 12/05/2018
ms.keywords: '*PEMRARC, *PEMRARCTO, *PEMRCHORD, *PEMRPIE, EMRARC, EMRARC structure [Windows GDI], EMRARC,EMRARCTO,EMRCHORD,EMRPIE, EMRARC,EMRARCTO,EMRCHORD,EMRPIE structure [Windows GDI], EMRARCTO, EMRARCTO structure [Windows GDI], EMRCHORD, EMRCHORD structure [Windows GDI], EMRPIE, EMRPIE structure [Windows GDI], PEMRARC, PEMRARC structure pointer [Windows GDI], PEMRARCTO, PEMRARCTO structure pointer [Windows GDI], PEMRCHORD, PEMRCHORD structure pointer [Windows GDI], PEMRPIE, PEMRPIE structure pointer [Windows GDI], _win32_EMRARC_str, gdi.emrarc__emrarcto__emrchord__emrpie, wingdi/EMRARC,EMRARCTO,EMRCHORD,EMRPIE, wingdi/EMRARCTO, wingdi/EMRCHORD, wingdi/EMRPIE, wingdi/PEMRARC, wingdi/PEMRARCTO, wingdi/PEMRCHORD, wingdi/PEMRPIE'
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
req.typenames: EMRARC, *PEMRARC, EMRARCTO, *PEMRARCTO, EMRCHORD, *PEMRCHORD, EMRPIE, *PEMRPIE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRARC
 - wingdi/tagEMRARC
 - PEMRARC
 - wingdi/PEMRARC
 - EMRARC
 - wingdi/EMRARC
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
 - EMRARC
---

# EMRARC structure


## -description

The <b>EMRARC, </b><b>EMRARCTO, </b><b>EMRCHORD, </b> and <b>EMRPIE</b> structures contain members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-arc">Arc</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-arcto">ArcTo</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-chord">Chord</a>, and <a href="/windows/desktop/api/wingdi/nf-wingdi-pie">Pie</a> enhanced metafile records.

## -struct-fields

### -field emr

Base structure for all record types.

### -field rclBox

Bounding rectangle in logical units.

### -field ptlStart

Coordinates of first radial ending point in logical units.

### -field ptlEnd

Coordinates of second radial ending point in logical units.

## -see-also

<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>