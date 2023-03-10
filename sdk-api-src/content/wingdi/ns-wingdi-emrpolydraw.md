---
UID: NS:wingdi.tagEMRPOLYDRAW
title: EMRPOLYDRAW (wingdi.h)
description: The EMRPOLYDRAW structure contains members for the PolyDraw enhanced metafile record.
helpviewer_keywords: ["*PEMRPOLYDRAW","EMRPOLYDRAW","EMRPOLYDRAW structure [Windows GDI]","PEMRPOLYDRAW","PEMRPOLYDRAW structure pointer [Windows GDI]","_win32_EMRPOLYDRAW_str","gdi.emrpolydraw","wingdi/EMRPOLYDRAW","wingdi/PEMRPOLYDRAW"]
old-location: gdi\emrpolydraw.htm
tech.root: gdi
ms.assetid: c75d19bf-a7e3-45db-9534-f089d4cec3eb
ms.date: 12/05/2018
ms.keywords: '*PEMRPOLYDRAW, EMRPOLYDRAW, EMRPOLYDRAW structure [Windows GDI], PEMRPOLYDRAW, PEMRPOLYDRAW structure pointer [Windows GDI], _win32_EMRPOLYDRAW_str, gdi.emrpolydraw, wingdi/EMRPOLYDRAW, wingdi/PEMRPOLYDRAW'
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
req.typenames: EMRPOLYDRAW, *PEMRPOLYDRAW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRPOLYDRAW
 - wingdi/tagEMRPOLYDRAW
 - PEMRPOLYDRAW
 - wingdi/PEMRPOLYDRAW
 - EMRPOLYDRAW
 - wingdi/EMRPOLYDRAW
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
 - EMRPOLYDRAW
---

# EMRPOLYDRAW structure


## -description

The <b>EMRPOLYDRAW</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-polydraw">PolyDraw</a> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field rclBounds

The bounding rectangle, in device units.

### -field cptl

The number of points.

### -field aptl

An array of <a href="/windows/win32/api/windef/ns-windef-pointl">POINTL</a> structures, representing the data points in logical units.

### -field abTypes

An array of values that specifies how each point in the <b>aptl</b> array is used. Each element can be one of the following values: PT_MOVETO, PT_LINETO, or PT_BEZIERTO. The PT_LINETO or PT_BEZIERTO value can be combined with the PT_CLOSEFIGURE value using the bitwise-OR operator.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-emr">EMR</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/win32/api/windef/ns-windef-pointl">POINTL</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polydraw">PolyDraw</a>



<a href="/windows/win32/api/windef/ns-windef-rectl">RECTL</a>