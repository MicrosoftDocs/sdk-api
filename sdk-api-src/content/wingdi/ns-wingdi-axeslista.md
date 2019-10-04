---
UID: NS:wingdi.tagAXESLISTA
title: AXESLISTA (wingdi.h)
author: windows-sdk-content
description: The AXESLIST structure contains information on all the axes of a multiple master font.
old-location: gdi\axeslist.htm
tech.root: gdi
ms.assetid: f95f012e-f02b-46c1-94ba-69f426ee7ad9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPAXESLISTA, *PAXESLISTA, AXESLIST, AXESLIST structure [Windows GDI], AXESLISTA, AXESLISTW, PAXESLIST, PAXESLIST structure pointer [Windows GDI], _win32_AXESLIST_str, gdi.axeslist, wingdi/AXESLIST, wingdi/AXESLISTA, wingdi/AXESLISTW, wingdi/PAXESLIST"
ms.topic: struct
f1_keywords: 
 - "wingdi/AXESLIST"
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
req.unicode-ansi: AXESLISTW (Unicode) and AXESLISTA (ANSI)
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
 - AXESLIST
 - AXESLISTA
 - AXESLISTW
targetos: Windows
req.typenames: AXESLISTA, *PAXESLISTA, *LPAXESLISTA
req.redist: 
ms.custom: 19H1
---

# AXESLISTA structure


## -description



The <b>AXESLIST</b> structure contains information on all the axes of a multiple master font.




## -struct-fields




### -field axlReserved

Reserved. Must be STAMP_AXESLIST.


### -field axlNumAxes

Number of axes for a specified multiple master font.


### -field axlAxisInfo

An array of <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-axisinfoa">AXISINFO</a> structures. Each <b>AXISINFO</b> structure contains information on an axis of a specified multiple master font. This corresponds to the <b>dvValues</b> array in the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-designvector">DESIGNVECTOR</a> structure.


## -remarks



The PostScript Open Type Font does not support multiple master functionality.

The information on the axes of a multiple master font are specified by the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-axisinfoa">AXISINFO</a> structures. The <b>axlNumAxes</b> member specifies the actual size of <b>axlAxisInfo</b>, while MM_MAX_NUMAXES, which equals 16, is the maximum allowed size of <b>axlAxisInfo</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-axisinfoa">AXISINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-designvector">DESIGNVECTOR</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-enumtextmetrica">ENUMTEXTMETRIC</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>
 

 

