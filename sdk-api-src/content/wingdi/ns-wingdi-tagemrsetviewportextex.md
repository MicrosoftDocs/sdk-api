---
UID: NS:wingdi.tagEMRSETVIEWPORTEXTEX
title: tagEMRSETVIEWPORTEXTEX
author: windows-sdk-content
description: The EMRSETVIEWPORTEXTEX and EMRSETWINDOWEXTEX structures contains members for the SetViewportExtEx and SetWindowExtEx enhanced metafile records.
old-location: gdi\emrsetviewportextex__emrsetwindowextex.htm
tech.root: gdi
ms.assetid: 4030c4c4-60be-43b7-855e-49d65ea482c1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PEMRSETVIEWPORTEXTEX, *PEMRSETWINDOWEXTEX, EMRSETVIEWPORTEXTEX, EMRSETVIEWPORTEXTEX structure [Windows GDI], EMRSETVIEWPORTEXTEX,EMRSETWINDOWEXTEX, EMRSETVIEWPORTEXTEX,EMRSETWINDOWEXTEX structure [Windows GDI], EMRSETWINDOWEXTEX, EMRSETWINDOWEXTEX structure [Windows GDI], PEMRSETVIEWPORTEXTEX, PEMRSETVIEWPORTEXTEX structure pointer [Windows GDI], PEMRSETWINDOWEXTEX, PEMRSETWINDOWEXTEX structure pointer [Windows GDI], _win32_EMRSETVIEWPORTEXTEX_str, gdi.emrsetviewportextex__emrsetwindowextex, tagEMRSETVIEWPORTEXTEX, wingdi/EMRSETVIEWPORTEXTEX,EMRSETWINDOWEXTEX, wingdi/EMRSETWINDOWEXTEX, wingdi/PEMRSETVIEWPORTEXTEX, wingdi/PEMRSETWINDOWEXTEX"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - EMRSETVIEWPORTEXTEX
product: Windows
targetos: Windows
req.typenames: EMRSETVIEWPORTEXTEX, *PEMRSETVIEWPORTEXTEX, EMRSETWINDOWEXTEX, *PEMRSETWINDOWEXTEX
req.redist: 
---

# tagEMRSETVIEWPORTEXTEX structure


## -description



The <b>EMRSETVIEWPORTEXTEX</b> and <b>EMRSETWINDOWEXTEX</b> structures contains members for the <b>SetViewportExtEx</b> and <b>SetWindowExtEx</b> enhanced metafile records.




## -struct-fields




### -field emr

Base structure for all record types.


### -field szlExtent

Horizontal and vertical extents. For <b>SetViewportExtEx</b>, the extents are in device units, and for <b>SetWindowExtEx</b>, the extents are in logical units.


## -see-also




<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

