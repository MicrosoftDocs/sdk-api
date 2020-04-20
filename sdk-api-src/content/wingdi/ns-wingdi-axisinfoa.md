---
UID: NS:wingdi.tagAXISINFOA
title: AXISINFOA (wingdi.h)
description: The AXISINFO structure contains information about an axis of a multiple master font.helpviewer_keywords: ["*LPAXISINFOA","*PAXISINFOA","AXISINFO","AXISINFO structure [Windows GDI]","AXISINFOA","AXISINFOW","PAXISINFO","PAXISINFO structure pointer [Windows GDI]","_win32_AXISINFO_str","gdi.axisinfo","wingdi/AXISINFO","wingdi/AXISINFOA","wingdi/AXISINFOW","wingdi/PAXISINFO"]
old-location: gdi\axisinfo.htm
tech.root: gdi
ms.assetid: a947618e-4b50-453a-82d5-5a6f825faebb
ms.date: 12/05/2018
ms.keywords: '*LPAXISINFOA, *PAXISINFOA, AXISINFO, AXISINFO structure [Windows GDI], AXISINFOA, AXISINFOW, PAXISINFO, PAXISINFO structure pointer [Windows GDI], _win32_AXISINFO_str, gdi.axisinfo, wingdi/AXISINFO, wingdi/AXISINFOA, wingdi/AXISINFOW, wingdi/PAXISINFO'
f1_keywords:
- wingdi/AXISINFO
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
req.unicode-ansi: AXISINFOW (Unicode) and AXISINFOA (ANSI)
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
- AXISINFO
- AXISINFOA
- AXISINFOW
targetos: Windows
req.typenames: AXISINFOA, *PAXISINFOA, *LPAXISINFOA
req.redist: 
ms.custom: 19H1
---

# AXISINFOA structure


## -description



The <b>AXISINFO</b> structure contains information about an axis of a multiple master font.




## -struct-fields




### -field axMinValue

The minimum value for this axis.


### -field axMaxValue

The maximum value for this axis.


### -field axAxisName

The name of the axis, specified as an array of characters.


## -remarks



The <b>AXISINFO</b> structure contains the name of an axis in a multiple master font and also the minimum and maximum possible values for the axis. The length of the name is MM_MAX_AXES_NAMELEN, which equals 16. An application queries these values before setting its desired values in the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-designvector">DESIGNVECTOR</a> array.

The PostScript Open Type Font does not support multiple master functionality.

For the ANSI version of this structure, <b>axAxisName</b> must be an array of bytes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-axeslista">AXESLIST</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-designvector">DESIGNVECTOR</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>
 

 

