---
UID: NS:wingdi.tagTTPOLYGONHEADER
title: tagTTPOLYGONHEADER
author: windows-sdk-content
description: The TTPOLYGONHEADER structure specifies the starting position and type of a contour in a TrueType character outline.
old-location: gdi\ttpolygonheader.htm
tech.root: gdi
ms.assetid: eea54aeb-7847-4393-87fa-86de93017be8
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*LPTTPOLYGONHEADER, LPTTPOLYGONHEADER, LPTTPOLYGONHEADER structure pointer [Windows GDI], TTPOLYGONHEADER, TTPOLYGONHEADER structure [Windows GDI], _win32_TTPOLYGONHEADER_str, gdi.ttpolygonheader, tagTTPOLYGONHEADER, wingdi/LPTTPOLYGONHEADER, wingdi/TTPOLYGONHEADER"
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
 - TTPOLYGONHEADER
product: Windows
targetos: Windows
req.typenames: TTPOLYGONHEADER, *LPTTPOLYGONHEADER
req.redist: 
---

# tagTTPOLYGONHEADER structure


## -description



The <b>TTPOLYGONHEADER</b> structure specifies the starting position and type of a contour in a TrueType character outline.




## -struct-fields




### -field cb

The number of bytes required by the <b>TTPOLYGONHEADER</b> structure and <a href="https://msdn.microsoft.com/59a26aec-786e-471b-8e08-ddffb04874d6">TTPOLYCURVE</a> structure or structures required to describe the contour of the character.


### -field dwType

The type of character outline returned. Currently, this value must be TT_POLYGON_TYPE.


### -field pfxStart

The starting point of the contour in the character outline.


## -remarks



Each <b>TTPOLYGONHEADER</b> structure is followed by one or more <a href="https://msdn.microsoft.com/59a26aec-786e-471b-8e08-ddffb04874d6">TTPOLYCURVE</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/a8736c6c-7944-42ed-811c-308f41f1ab2f">POINTFX</a>



<a href="https://msdn.microsoft.com/59a26aec-786e-471b-8e08-ddffb04874d6">TTPOLYCURVE</a>
 

 

