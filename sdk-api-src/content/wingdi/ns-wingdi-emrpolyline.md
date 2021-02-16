---
UID: NS:wingdi.tagEMRPOLYLINE
title: EMRPOLYLINE (wingdi.h)
description: The EMRPOLYLINE, EMRPOLYBEZIER, EMRPOLYGON, EMRPOLYBEZIERTO, and EMRPOLYLINETO structures contain members for the Polyline, PolyBezier, Polygon, PolyBezierTo, and PolylineTo enhanced metafile records.
helpviewer_keywords: ["*PEMRPOLYBEZIER","*PEMRPOLYBEZIERTO","*PEMRPOLYGON","*PEMRPOLYLINE","*PEMRPOLYLINETO","EMRPOLYBEZIER","EMRPOLYBEZIER structure [Windows GDI]","EMRPOLYBEZIERTO","EMRPOLYBEZIERTO structure [Windows GDI]","EMRPOLYGON","EMRPOLYGON structure [Windows GDI]","EMRPOLYLINE","EMRPOLYLINE structure [Windows GDI]","EMRPOLYLINE","EMRPOLYBEZIER","EMRPOLYGON","EMRPOLYBEZIERTO","EMRPOLYLINETO","EMRPOLYLINE","EMRPOLYBEZIER","EMRPOLYGON","EMRPOLYBEZIERTO","EMRPOLYLINETO structure [Windows GDI]","EMRPOLYLINETO","EMRPOLYLINETO structure [Windows GDI]","PEMRPOLYBEZIER","PEMRPOLYBEZIER structure pointer [Windows GDI]","PEMRPOLYBEZIERTO","PEMRPOLYBEZIERTO structure pointer [Windows GDI]","PEMRPOLYGON","PEMRPOLYGON structure pointer [Windows GDI]","PEMRPOLYLINE","PEMRPOLYLINE structure pointer [Windows GDI]","PEMRPOLYLINETO","PEMRPOLYLINETO structure pointer [Windows GDI]","_win32_EMRPOLYLINE_str","gdi.emrpolyline__emrpolybezier__emrpolygon__emrpolybezierto__emrpolylineto","wingdi/EMRPOLYBEZIER","wingdi/EMRPOLYBEZIERTO","wingdi/EMRPOLYGON","wingdi/EMRPOLYLINE","EMRPOLYBEZIER","EMRPOLYGON","EMRPOLYBEZIERTO","EMRPOLYLINETO","wingdi/EMRPOLYLINETO","wingdi/PEMRPOLYBEZIER","wingdi/PEMRPOLYBEZIERTO","wingdi/PEMRPOLYGON","wingdi/PEMRPOLYLINE","wingdi/PEMRPOLYLINETO"]
old-location: gdi\emrpolyline__emrpolybezier__emrpolygon__emrpolybezierto__emrpolylineto.htm
tech.root: gdi
ms.assetid: 47a05287-8950-4277-b981-a19bff918bae
ms.date: 12/05/2018
ms.keywords: '*PEMRPOLYBEZIER, *PEMRPOLYBEZIERTO, *PEMRPOLYGON, *PEMRPOLYLINE, *PEMRPOLYLINETO, EMRPOLYBEZIER, EMRPOLYBEZIER structure [Windows GDI], EMRPOLYBEZIERTO, EMRPOLYBEZIERTO structure [Windows GDI], EMRPOLYGON, EMRPOLYGON structure [Windows GDI], EMRPOLYLINE, EMRPOLYLINE structure [Windows GDI], EMRPOLYLINE,EMRPOLYBEZIER,EMRPOLYGON,EMRPOLYBEZIERTO,EMRPOLYLINETO, EMRPOLYLINE,EMRPOLYBEZIER,EMRPOLYGON,EMRPOLYBEZIERTO,EMRPOLYLINETO structure [Windows GDI], EMRPOLYLINETO, EMRPOLYLINETO structure [Windows GDI], PEMRPOLYBEZIER, PEMRPOLYBEZIER structure pointer [Windows GDI], PEMRPOLYBEZIERTO, PEMRPOLYBEZIERTO structure pointer [Windows GDI], PEMRPOLYGON, PEMRPOLYGON structure pointer [Windows GDI], PEMRPOLYLINE, PEMRPOLYLINE structure pointer [Windows GDI], PEMRPOLYLINETO, PEMRPOLYLINETO structure pointer [Windows GDI], _win32_EMRPOLYLINE_str, gdi.emrpolyline__emrpolybezier__emrpolygon__emrpolybezierto__emrpolylineto, wingdi/EMRPOLYBEZIER, wingdi/EMRPOLYBEZIERTO, wingdi/EMRPOLYGON, wingdi/EMRPOLYLINE,EMRPOLYBEZIER,EMRPOLYGON,EMRPOLYBEZIERTO,EMRPOLYLINETO, wingdi/EMRPOLYLINETO, wingdi/PEMRPOLYBEZIER, wingdi/PEMRPOLYBEZIERTO, wingdi/PEMRPOLYGON, wingdi/PEMRPOLYLINE, wingdi/PEMRPOLYLINETO'
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
req.typenames: EMRPOLYLINE, *PEMRPOLYLINE, EMRPOLYBEZIER, *PEMRPOLYBEZIER, EMRPOLYGON, *PEMRPOLYGON, EMRPOLYBEZIERTO, *PEMRPOLYBEZIERTO, EMRPOLYLINETO, *PEMRPOLYLINETO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRPOLYLINE
 - wingdi/tagEMRPOLYLINE
 - PEMRPOLYLINE
 - wingdi/PEMRPOLYLINE
 - EMRPOLYLINE
 - wingdi/EMRPOLYLINE
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
 - EMRPOLYLINE
---

# EMRPOLYLINE structure


## -description

The <b>EMRPOLYLINE, </b><b>EMRPOLYBEZIER, </b><b>EMRPOLYGON, </b><b>EMRPOLYBEZIERTO, </b> and <b>EMRPOLYLINETO</b> structures contain members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-polyline">Polyline</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-polybezier">PolyBezier</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-polygon">Polygon</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-polybezierto">PolyBezierTo</a>, and <a href="/windows/desktop/api/wingdi/nf-wingdi-polylineto">PolylineTo</a> enhanced metafile records.

## -struct-fields

### -field emr

Base structure for all record types.

### -field rclBounds

Bounding rectangle, in device units.

### -field cptl

Number of points array.

### -field aptl

Array of 32-bit points, in logical units.

## -see-also

<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>