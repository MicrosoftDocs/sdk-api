---
UID: NS:wingdi.tagAXESLISTA
title: AXESLISTA (wingdi.h)
author: windows-sdk-content
description: The AXESLIST structure contains information on all the axes of a multiple master font.
old-location: gdi\axeslist.htm
tech.root: gdi
ms.assetid: f95f012e-f02b-46c1-94ba-69f426ee7ad9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPAXESLISTA, *PAXESLISTA, AXESLIST, AXESLIST structure [Windows GDI], AXESLISTA, AXESLISTW, PAXESLIST, PAXESLIST structure pointer [Windows GDI], _win32_AXESLIST_str, gdi.axeslist, wingdi/AXESLIST, wingdi/AXESLISTA, wingdi/AXESLISTW, wingdi/PAXESLIST"
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: AXESLISTA, *PAXESLISTA, *LPAXESLISTA
req.redist: 
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

An array of <a href="https://msdn.microsoft.com/a947618e-4b50-453a-82d5-5a6f825faebb">AXISINFO</a> structures. Each <b>AXISINFO</b> structure contains information on an axis of a specified multiple master font. This corresponds to the <b>dvValues</b> array in the <a href="https://msdn.microsoft.com/aeff9901-2405-44aa-ba46-8d784afd6b76">DESIGNVECTOR</a> structure.


## -remarks



The PostScript Open Type Font does not support multiple master functionality.

The information on the axes of a multiple master font are specified by the <a href="https://msdn.microsoft.com/a947618e-4b50-453a-82d5-5a6f825faebb">AXISINFO</a> structures. The <b>axlNumAxes</b> member specifies the actual size of <b>axlAxisInfo</b>, while MM_MAX_NUMAXES, which equals 16, is the maximum allowed size of <b>axlAxisInfo</b>.




## -see-also




<a href="https://msdn.microsoft.com/a947618e-4b50-453a-82d5-5a6f825faebb">AXISINFO</a>



<a href="https://msdn.microsoft.com/aeff9901-2405-44aa-ba46-8d784afd6b76">DESIGNVECTOR</a>



<a href="https://msdn.microsoft.com/deb81846-3ada-4c88-8c26-74224538d282">ENUMTEXTMETRIC</a>



<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>
 

 

