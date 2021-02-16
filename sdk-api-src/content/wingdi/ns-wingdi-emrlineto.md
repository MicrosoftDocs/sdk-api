---
UID: NS:wingdi.tagEMRLINETO
title: EMRLINETO (wingdi.h)
description: The EMRLINETO and EMRMOVETOEX structures contains members for the LineTo and MoveToEx enhanced metafile records.
helpviewer_keywords: ["*PEMRLINETO","*PEMRMOVETOEX","EMRLINETO","EMRLINETO structure [Windows GDI]","EMRLINETO","EMRMOVETOEX","EMRLINETO","EMRMOVETOEX structure [Windows GDI]","EMRMOVETOEX","EMRMOVETOEX structure [Windows GDI]","PEMRLINETO","PEMRLINETO structure pointer [Windows GDI]","PEMRMOVETOEX","PEMRMOVETOEX structure pointer [Windows GDI]","_win32_EMRLINETO_str","gdi.emrlineto__emrmovetoex","wingdi/EMRLINETO","EMRMOVETOEX","wingdi/EMRMOVETOEX","wingdi/PEMRLINETO","wingdi/PEMRMOVETOEX"]
old-location: gdi\emrlineto__emrmovetoex.htm
tech.root: gdi
ms.assetid: 876db90d-3775-48e8-8911-e6612a3484ae
ms.date: 12/05/2018
ms.keywords: '*PEMRLINETO, *PEMRMOVETOEX, EMRLINETO, EMRLINETO structure [Windows GDI], EMRLINETO,EMRMOVETOEX, EMRLINETO,EMRMOVETOEX structure [Windows GDI], EMRMOVETOEX, EMRMOVETOEX structure [Windows GDI], PEMRLINETO, PEMRLINETO structure pointer [Windows GDI], PEMRMOVETOEX, PEMRMOVETOEX structure pointer [Windows GDI], _win32_EMRLINETO_str, gdi.emrlineto__emrmovetoex, wingdi/EMRLINETO,EMRMOVETOEX, wingdi/EMRMOVETOEX, wingdi/PEMRLINETO, wingdi/PEMRMOVETOEX'
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
req.typenames: EMRLINETO, *PEMRLINETO, EMRMOVETOEX, *PEMRMOVETOEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRLINETO
 - wingdi/tagEMRLINETO
 - PEMRLINETO
 - wingdi/PEMRLINETO
 - EMRLINETO
 - wingdi/EMRLINETO
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
 - EMRLINETO
---

# EMRLINETO structure


## -description

The <b>EMRLINETO</b> and <b>EMRMOVETOEX</b> structures contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-lineto">LineTo</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-movetoex">MoveToEx</a> enhanced metafile records.

## -struct-fields

### -field emr

Base structure for all record types.

### -field ptl

Coordinates of the line's ending point for the <a href="/windows/desktop/api/wingdi/nf-wingdi-lineto">LineTo</a> function or coordinates of the new current position for the <a href="/windows/desktop/api/wingdi/nf-wingdi-movetoex">MoveToEx</a> function in logical units.

## -see-also

<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>