---
UID: NS:wingdi.tagEMRLINETO
title: tagEMRLINETO
author: windows-sdk-content
description: The EMRLINETO and EMRMOVETOEX structures contains members for the LineTo and MoveToEx enhanced metafile records.
old-location: gdi\emrlineto__emrmovetoex.htm
tech.root: gdi
ms.assetid: 876db90d-3775-48e8-8911-e6612a3484ae
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PEMRLINETO, *PEMRMOVETOEX, EMRLINETO, EMRLINETO structure [Windows GDI], EMRLINETO,EMRMOVETOEX, EMRLINETO,EMRMOVETOEX structure [Windows GDI], EMRMOVETOEX, EMRMOVETOEX structure [Windows GDI], PEMRLINETO, PEMRLINETO structure pointer [Windows GDI], PEMRMOVETOEX, PEMRMOVETOEX structure pointer [Windows GDI], _win32_EMRLINETO_str, gdi.emrlineto__emrmovetoex, tagEMRLINETO, wingdi/EMRLINETO,EMRMOVETOEX, wingdi/EMRMOVETOEX, wingdi/PEMRLINETO, wingdi/PEMRMOVETOEX"
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
 - EMRLINETO
product: Windows
targetos: Windows
req.typenames: EMRLINETO, *PEMRLINETO, EMRMOVETOEX, *PEMRMOVETOEX
req.redist: 
---

# tagEMRLINETO structure


## -description



The <b>EMRLINETO</b> and <b>EMRMOVETOEX</b> structures contains members for the <a href="https://msdn.microsoft.com/a31b3a9a-110f-4cdf-89d9-19937a2e40b4">LineTo</a> and <a href="https://msdn.microsoft.com/af11eeb7-4036-4a90-8685-9b5719f79e01">MoveToEx</a> enhanced metafile records.




## -struct-fields




### -field emr

Base structure for all record types.


### -field ptl

Coordinates of the line's ending point for the <a href="https://msdn.microsoft.com/a31b3a9a-110f-4cdf-89d9-19937a2e40b4">LineTo</a> function or coordinates of the new current position for the <a href="https://msdn.microsoft.com/af11eeb7-4036-4a90-8685-9b5719f79e01">MoveToEx</a> function in logical units.


## -see-also




<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

