---
UID: NS:wingdi._RGNDATA
title: RGNDATA (wingdi.h)
author: windows-sdk-content
description: The RGNDATA structure contains a header and an array of rectangles that compose a region. The rectangles are sorted top to bottom, left to right. They do not overlap.
old-location: gdi\rgndata.htm
tech.root: gdi
ms.assetid: 3eac0b23-3138-4b34-9c16-6cc185e4de22
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*LPRGNDATA, *NPRGNDATA, *PRGNDATA, PRGNDATA, PRGNDATA structure pointer [Windows GDI], RGNDATA, RGNDATA structure [Windows GDI], _RGNDATA, _win32_RGNDATA_str, gdi.rgndata, wingdi/PRGNDATA, wingdi/RGNDATA'
ms.topic: struct
f1_keywords:
- wingdi/RGNDATA
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
- RGNDATA
targetos: Windows
req.typenames: RGNDATA, *PRGNDATA, *NPRGNDATA, *LPRGNDATA
req.redist: 
ms.custom: 19H1
---

# RGNDATA structure


## -description



The <b>RGNDATA</b> structure contains a header and an array of rectangles that compose a region. The rectangles are sorted top to bottom, left to right. They do not overlap.




## -struct-fields




### -field rdh

A <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-rgndataheader">RGNDATAHEADER</a> structure. The members of this structure specify the type of region (whether it is rectangular or trapezoidal), the number of rectangles that make up the region, the size of the buffer that contains the rectangle structures, and so on.


### -field Buffer

Specifies an arbitrary-size buffer that contains the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structures that make up the region.


## -see-also




<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-rgndataheader">RGNDATAHEADER</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/region-structures">Region Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/regions">Regions Overview</a>
 

 

