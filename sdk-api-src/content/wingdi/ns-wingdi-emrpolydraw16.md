---
UID: NS:wingdi.tagEMRPOLYDRAW16
title: EMRPOLYDRAW16 (wingdi.h)
author: windows-sdk-content
description: The EMRPOLYDRAW16 structure contains members for the PolyDraw enhanced metafile record.
old-location: gdi\emrpolydraw16.htm
tech.root: gdi
ms.assetid: 476c5a81-99fc-4e25-a761-b95bbf18b271
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PEMRPOLYDRAW16, EMRPOLYDRAW16, EMRPOLYDRAW16 structure [Windows GDI], PEMRPOLYDRAW16, PEMRPOLYDRAW16 structure pointer [Windows GDI], _win32_EMRPOLYDRAW16_str, gdi.emrpolydraw16, wingdi/EMRPOLYDRAW16, wingdi/PEMRPOLYDRAW16"
ms.topic: struct
f1_keywords: 
 - "wingdi/EMRPOLYDRAW16"
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
 - EMRPOLYDRAW16
targetos: Windows
req.typenames: EMRPOLYDRAW16, *PEMRPOLYDRAW16
req.redist: 
ms.custom: 19H1
---

# EMRPOLYDRAW16 structure


## -description



The <b>EMRPOLYDRAW16</b> structure contains members for the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-polydraw">PolyDraw</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field rclBounds

The bounding rectangle, in device units.


### -field cpts

The number of points.


### -field apts

An array of <a href="https://docs.microsoft.com/previous-versions/dd162808(v=vs.85)">POINTS</a> structures, representing the data points in logical units.


### -field abTypes

An array of values that specifies how each point in the <b>apts</b> array is used. Each element can be one of the following values: PT_MOVETO, PT_LINETO, or PT_BEZIERTO. The PT_LINETO or PT_BEZIERTO value can be combined with the PT_CLOSEFIGURE value using the bitwise-OR operator.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-emr">EMR</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="https://docs.microsoft.com/previous-versions/dd162808(v=vs.85)">POINTS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-polydraw">PolyDraw</a>



<a href="https://docs.microsoft.com/previous-versions/dd162907(v=vs.85)">RECTL</a>
 

 

