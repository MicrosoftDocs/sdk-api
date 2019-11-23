---
UID: NS:wingdi.tagEMRPOLYPOLYLINE
title: EMRPOLYPOLYLINE (wingdi.h)

description: The EMRPOLYPOLYLINE and EMRPOLYPOLYGON structures contain members for the PolyPolyline and PolyPolygon enhanced metafile records.
old-location: gdi\emrpolypolyline__emrpolypolygon.htm
tech.root: gdi
ms.assetid: 442ad347-c064-4769-b43b-57d2e66e8b97

ms.date: 12/05/2018
ms.keywords: "*PEMRPOLYPOLYGON, *PEMRPOLYPOLYLINE, EMRPOLYPOLYGON, EMRPOLYPOLYGON structure [Windows GDI], EMRPOLYPOLYLINE, EMRPOLYPOLYLINE structure [Windows GDI], EMRPOLYPOLYLINE,EMRPOLYPOLYGON, EMRPOLYPOLYLINE,EMRPOLYPOLYGON structure [Windows GDI], PEMRPOLYPOLYGON, PEMRPOLYPOLYGON structure pointer [Windows GDI], PEMRPOLYPOLYLINE, PEMRPOLYPOLYLINE structure pointer [Windows GDI], _win32_EMRPOLYPOLYLINE_str, gdi.emrpolypolyline__emrpolypolygon, wingdi/EMRPOLYPOLYGON, wingdi/EMRPOLYPOLYLINE,EMRPOLYPOLYGON, wingdi/PEMRPOLYPOLYGON, wingdi/PEMRPOLYPOLYLINE"
ms.topic: struct
f1_keywords: 
 - "wingdi/EMRPOLYPOLYLINE"
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
 - EMRPOLYPOLYLINE
targetos: Windows
req.typenames: EMRPOLYPOLYLINE, *PEMRPOLYPOLYLINE, EMRPOLYPOLYGON, *PEMRPOLYPOLYGON
req.redist: 
ms.custom: 19H1
---

# EMRPOLYPOLYLINE structure


## -description



The <b>EMRPOLYPOLYLINE</b> and <b>EMRPOLYPOLYGON</b> structures contain members for the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-polypolyline">PolyPolyline</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-polypolygon">PolyPolygon</a> enhanced metafile records.




## -struct-fields




### -field emr

The base structure for all record types.


### -field rclBounds

The bounding rectangle, in device units.


### -field nPolys

The number of polys.


### -field cptl

The total number of points in all polys.


### -field aPolyCounts

An array of point counts for each poly.


### -field aptl

An array of <a href="https://docs.microsoft.com/previous-versions/dd162807(v=vs.85)">POINTL</a> structures, representing the points in logical units.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-emr">EMR</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="https://docs.microsoft.com/previous-versions/dd162807(v=vs.85)">POINTL</a>



<a href="https://docs.microsoft.com/previous-versions/dd162907(v=vs.85)">RECTL</a>
 

 

