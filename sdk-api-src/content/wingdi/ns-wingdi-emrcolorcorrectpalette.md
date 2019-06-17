---
UID: NS:wingdi.tagCOLORCORRECTPALETTE
title: EMRCOLORCORRECTPALETTE (wingdi.h)
author: windows-sdk-content
description: The EMRCOLORCORRECTPALETTE structure contains members for the ColorCorrectPalette enhanced metafile record.
old-location: gdi\emrcolorcorrectpalette.htm
tech.root: gdi
ms.assetid: 12e31e22-b9ac-454d-a423-b3fee582fcba
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PEMRCOLORCORRECTPALETTE, EMRCOLORCORRECTPALETTE, EMRCOLORCORRECTPALETTE structure [Windows GDI], PEMRCOLORCORRECTPALETTE, PEMRCOLORCORRECTPALETTE structure pointer [Windows GDI], _win32_EMRCOLORCORRECTPALETTE_str, gdi.emrcolorcorrectpalette, wingdi/EMRCOLORCORRECTPALETTE, wingdi/PEMRCOLORCORRECTPALETTE"
ms.topic: struct
f1_keywords: ["wingdi/EMRCOLORCORRECTPALETTE"]
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
 - EMRCOLORCORRECTPALETTE
product: Windows
targetos: Windows
req.typenames: EMRCOLORCORRECTPALETTE, *PEMRCOLORCORRECTPALETTE
req.redist: 
ms.custom: 19H1
---

# EMRCOLORCORRECTPALETTE structure


## -description



The <b>EMRCOLORCORRECTPALETTE</b> structure contains members for the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-colorcorrectpalette">ColorCorrectPalette</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field ihPalette

The index of the palette handle to color correct.


### -field nFirstEntry

The index of the first entry in the palette to color correct.


### -field nPalEntries

The number of palette entries to color correct.


### -field nReserved

Reserved.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-colorcorrectpalette">ColorCorrectPalette</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafiles">Metafiles Overview</a>
 

 

