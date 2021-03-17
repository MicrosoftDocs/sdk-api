---
UID: NS:wingdi.tagEMRANGLEARC
title: EMRANGLEARC (wingdi.h)
description: The EMRANGLEARC structure contains members for the AngleArc enhanced metafile record.
helpviewer_keywords: ["*PEMRANGLEARC","EMRANGLEARC","EMRANGLEARC structure [Windows GDI]","PEMRANGLEARC","PEMRANGLEARC structure pointer [Windows GDI]","_win32_EMRANGLEARC_str","gdi.emranglearc","wingdi/EMRANGLEARC","wingdi/PEMRANGLEARC"]
old-location: gdi\emranglearc.htm
tech.root: gdi
ms.assetid: 054b84ba-bb5e-4dca-8482-6b958151aedf
ms.date: 12/05/2018
ms.keywords: '*PEMRANGLEARC, EMRANGLEARC, EMRANGLEARC structure [Windows GDI], PEMRANGLEARC, PEMRANGLEARC structure pointer [Windows GDI], _win32_EMRANGLEARC_str, gdi.emranglearc, wingdi/EMRANGLEARC, wingdi/PEMRANGLEARC'
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
req.typenames: EMRANGLEARC, *PEMRANGLEARC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRANGLEARC
 - wingdi/tagEMRANGLEARC
 - PEMRANGLEARC
 - wingdi/PEMRANGLEARC
 - EMRANGLEARC
 - wingdi/EMRANGLEARC
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
 - EMRANGLEARC
---

# EMRANGLEARC structure


## -description

The <b>EMRANGLEARC</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-anglearc">AngleArc</a> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field ptlCenter

Logical coordinates of a circle's center.

### -field nRadius

A circle's radius, in logical units.

### -field eStartAngle

An arc's start angle, in degrees.

### -field eSweepAngle

An arc's sweep angle, in degrees.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-anglearc">AngleArc</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>