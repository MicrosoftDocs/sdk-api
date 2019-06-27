---
UID: NS:wingdi.tagEMRPOLYDRAW
title: EMRPOLYDRAW (wingdi.h)
author: windows-sdk-content
description: The EMRPOLYDRAW structure contains members for the PolyDraw enhanced metafile record.
old-location: gdi\emrpolydraw.htm
tech.root: gdi
ms.assetid: c75d19bf-a7e3-45db-9534-f089d4cec3eb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PEMRPOLYDRAW, EMRPOLYDRAW, EMRPOLYDRAW structure [Windows GDI], PEMRPOLYDRAW, PEMRPOLYDRAW structure pointer [Windows GDI], _win32_EMRPOLYDRAW_str, gdi.emrpolydraw, wingdi/EMRPOLYDRAW, wingdi/PEMRPOLYDRAW"
ms.topic: struct
f1_keywords: 
 - "wingdi/EMRPOLYDRAW"
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
 - EMRPOLYDRAW
product: Windows
targetos: Windows
req.typenames: EMRPOLYDRAW, *PEMRPOLYDRAW
req.redist: 
ms.custom: 19H1
---

# EMRPOLYDRAW structure


## -description



The <b>EMRPOLYDRAW</b> structure contains members for the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-polydraw">PolyDraw</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field rclBounds

The bounding rectangle, in device units.


### -field cptl

The number of points.


### -field aptl

An array of <a href="https://docs.microsoft.com/previous-versions/dd162807(v=vs.85)">POINTL</a> structures, representing the data points in logical units.


### -field abTypes

An array of values that specifies how each point in the <b>aptl</b> array is used. Each element can be one of the following values: PT_MOVETO, PT_LINETO, or PT_BEZIERTO. The PT_LINETO or PT_BEZIERTO value can be combined with the PT_CLOSEFIGURE value using the bitwise-OR operator.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemr">EMR</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="https://docs.microsoft.com/previous-versions/dd162807(v=vs.85)">POINTL</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-polydraw">PolyDraw</a>



<a href="https://docs.microsoft.com/previous-versions/dd162907(v=vs.85)">RECTL</a>
 

 

