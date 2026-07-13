---
UID: NS:wingdi.tagEMRPOLYPOLYLINE16
title: EMRPOLYPOLYLINE16 (wingdi.h)
description: The EMRPOLYPOLYLINE16 and EMRPOLYPOLYGON16 structures contain members for the PolyPolyline and PolyPolygon enhanced metafile records.
helpviewer_keywords: ["*PEMRPOLYPOLYGON16","*PEMRPOLYPOLYLINE16","EMRPOLYPOLYGON16","EMRPOLYPOLYGON16 structure [Windows GDI]","EMRPOLYPOLYLINE16","EMRPOLYPOLYLINE16 structure [Windows GDI]","EMRPOLYPOLYLINE16","EMRPOLYPOLYGON16","EMRPOLYPOLYLINE16","EMRPOLYPOLYGON16 structure [Windows GDI]","PEMRPOLYPOLYGON16","PEMRPOLYPOLYGON16 structure pointer [Windows GDI]","PEMRPOLYPOLYLINE16","PEMRPOLYPOLYLINE16 structure pointer [Windows GDI]","_win32_EMRPOLYPOLYLINE16_str","gdi.emrpolypolyline16__emrpolypolygon16","wingdi/EMRPOLYPOLYGON16","wingdi/EMRPOLYPOLYLINE16","EMRPOLYPOLYGON16","wingdi/PEMRPOLYPOLYGON16","wingdi/PEMRPOLYPOLYLINE16"]
old-location: gdi\emrpolypolyline16__emrpolypolygon16.htm
tech.root: gdi
ms.assetid: efdd4ed1-5c0e-43ae-980d-fe3a5e8d480f
ms.date: 12/05/2018
ms.keywords: '*PEMRPOLYPOLYGON16, *PEMRPOLYPOLYLINE16, EMRPOLYPOLYGON16, EMRPOLYPOLYGON16 structure [Windows GDI], EMRPOLYPOLYLINE16, EMRPOLYPOLYLINE16 structure [Windows GDI], EMRPOLYPOLYLINE16,EMRPOLYPOLYGON16, EMRPOLYPOLYLINE16,EMRPOLYPOLYGON16 structure [Windows GDI], PEMRPOLYPOLYGON16, PEMRPOLYPOLYGON16 structure pointer [Windows GDI], PEMRPOLYPOLYLINE16, PEMRPOLYPOLYLINE16 structure pointer [Windows GDI], _win32_EMRPOLYPOLYLINE16_str, gdi.emrpolypolyline16__emrpolypolygon16, wingdi/EMRPOLYPOLYGON16, wingdi/EMRPOLYPOLYLINE16,EMRPOLYPOLYGON16, wingdi/PEMRPOLYPOLYGON16, wingdi/PEMRPOLYPOLYLINE16'
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
req.typenames: EMRPOLYPOLYLINE16, *PEMRPOLYPOLYLINE16, EMRPOLYPOLYGON16, *PEMRPOLYPOLYGON16
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRPOLYPOLYLINE16
 - wingdi/tagEMRPOLYPOLYLINE16
 - PEMRPOLYPOLYLINE16
 - wingdi/PEMRPOLYPOLYLINE16
 - EMRPOLYPOLYLINE16
 - wingdi/EMRPOLYPOLYLINE16
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
 - EMRPOLYPOLYLINE16
---

# EMRPOLYPOLYLINE16 structure


## -description

The <b>EMRPOLYPOLYLINE16</b> and <b>EMRPOLYPOLYGON16</b> structures contain members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-polypolyline">PolyPolyline</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-polypolygon">PolyPolygon</a> enhanced metafile records.

## -struct-fields

### -field emr

The base structure for all record types.

### -field rclBounds

The bounding rectangle, in device units.

### -field nPolys

The number of polys.

### -field cpts

The total number of points in all polys.

### -field aPolyCounts

An array of point counts for each poly.

### -field apts

An array of <a href="/windows/win32/api/windef/ns-windef-points">POINTS</a> structures, representing the points in logical units.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-emr">EMR</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/win32/api/windef/ns-windef-points">POINTS</a>



<a href="/windows/win32/api/windef/ns-windef-rectl">RECTL</a>