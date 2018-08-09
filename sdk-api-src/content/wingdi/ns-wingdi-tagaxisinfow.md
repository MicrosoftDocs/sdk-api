---
UID: NS:wingdi.tagAXISINFOW
title: tagAXISINFOW
author: windows-sdk-content
description: The AXISINFO structure contains information about an axis of a multiple master font.
old-location: gdi\axisinfo.htm
old-project: gdi
ms.assetid: a947618e-4b50-453a-82d5-5a6f825faebb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPAXISINFOW, *PAXISINFOW, AXISINFO, AXISINFO structure [Windows GDI], AXISINFOA, AXISINFOW, PAXISINFO, PAXISINFO structure pointer [Windows GDI], _win32_AXISINFO_str, gdi.axisinfo, tagAXISINFOW, wingdi/AXISINFO, wingdi/AXISINFOA, wingdi/AXISINFOW, wingdi/PAXISINFO"
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
req.unicode-ansi: AXISINFOW (Unicode) and AXISINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AXISINFOW, *PAXISINFOW, *LPAXISINFOW
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagAXISINFOW structure


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



The <b>AXISINFO</b> structure contains the name of an axis in a multiple master font and also the minimum and maximum possible values for the axis. The length of the name is MM_MAX_AXES_NAMELEN, which equals 16. An application queries these values before setting its desired values in the <a href="https://msdn.microsoft.com/aeff9901-2405-44aa-ba46-8d784afd6b76">DESIGNVECTOR</a> array.

The PostScript Open Type Font does not support multiple master functionality.

For the ANSI version of this structure, <b>axAxisName</b> must be an array of bytes.




## -see-also




<a href="https://msdn.microsoft.com/f95f012e-f02b-46c1-94ba-69f426ee7ad9">AXESLIST</a>



<a href="https://msdn.microsoft.com/aeff9901-2405-44aa-ba46-8d784afd6b76">DESIGNVECTOR</a>



<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>
 

 

