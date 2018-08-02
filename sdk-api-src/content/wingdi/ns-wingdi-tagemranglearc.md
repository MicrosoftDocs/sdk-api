---
UID: NS:wingdi.tagEMRANGLEARC
title: tagEMRANGLEARC
author: windows-sdk-content
description: The EMRANGLEARC structure contains members for the AngleArc enhanced metafile record.
old-location: gdi\emranglearc.htm
old-project: gdi
ms.assetid: 054b84ba-bb5e-4dca-8482-6b958151aedf
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PEMRANGLEARC, EMRANGLEARC, EMRANGLEARC structure [Windows GDI], PEMRANGLEARC, PEMRANGLEARC structure pointer [Windows GDI], _win32_EMRANGLEARC_str, gdi.emranglearc, tagEMRANGLEARC, wingdi/EMRANGLEARC, wingdi/PEMRANGLEARC"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: EMRANGLEARC, *PEMRANGLEARC
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagEMRANGLEARC structure


## -description



The <b>EMRANGLEARC</b> structure contains members for the <a href="https://msdn.microsoft.com/65c38da1-ab7d-4e80-83e3-ba1db66f8fd9">AngleArc</a> enhanced metafile record.




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




<a href="https://msdn.microsoft.com/65c38da1-ab7d-4e80-83e3-ba1db66f8fd9">AngleArc</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

