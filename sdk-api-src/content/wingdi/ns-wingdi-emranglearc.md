---
UID: NS:wingdi.tagEMRANGLEARC
title: EMRANGLEARC (wingdi.h)
author: windows-sdk-content
description: The EMRANGLEARC structure contains members for the AngleArc enhanced metafile record.
old-location: gdi\emranglearc.htm
tech.root: gdi
ms.assetid: 054b84ba-bb5e-4dca-8482-6b958151aedf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PEMRANGLEARC, EMRANGLEARC, EMRANGLEARC structure [Windows GDI], PEMRANGLEARC, PEMRANGLEARC structure pointer [Windows GDI], _win32_EMRANGLEARC_str, gdi.emranglearc, wingdi/EMRANGLEARC, wingdi/PEMRANGLEARC"
ms.topic: struct
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
 - EMRANGLEARC
product: Windows
targetos: Windows
req.typenames: EMRANGLEARC, *PEMRANGLEARC
req.redist: 
ms.custom: 19H1
---

# EMRANGLEARC structure


## -description



The <b>EMRANGLEARC</b> structure contains members for the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-anglearc">AngleArc</a> enhanced metafile record.




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




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-anglearc">AngleArc</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafiles">Metafiles Overview</a>
 

 

