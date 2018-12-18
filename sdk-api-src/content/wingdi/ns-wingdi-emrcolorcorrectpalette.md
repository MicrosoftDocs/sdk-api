---
UID: NS:wingdi.tagCOLORCORRECTPALETTE
title: EMRCOLORCORRECTPALETTE
author: windows-sdk-content
description: The EMRCOLORCORRECTPALETTE structure contains members for the ColorCorrectPalette enhanced metafile record.
old-location: gdi\emrcolorcorrectpalette.htm
tech.root: gdi
ms.assetid: 12e31e22-b9ac-454d-a423-b3fee582fcba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PEMRCOLORCORRECTPALETTE, EMRCOLORCORRECTPALETTE, EMRCOLORCORRECTPALETTE structure [Windows GDI], PEMRCOLORCORRECTPALETTE, PEMRCOLORCORRECTPALETTE structure pointer [Windows GDI], _win32_EMRCOLORCORRECTPALETTE_str, gdi.emrcolorcorrectpalette, wingdi/EMRCOLORCORRECTPALETTE, wingdi/PEMRCOLORCORRECTPALETTE"
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
 - EMRCOLORCORRECTPALETTE
product: Windows
targetos: Windows
req.typenames: EMRCOLORCORRECTPALETTE, *PEMRCOLORCORRECTPALETTE
req.redist: 
---

# EMRCOLORCORRECTPALETTE structure


## -description



The <b>EMRCOLORCORRECTPALETTE</b> structure contains members for the <a href="https://msdn.microsoft.com/e7680521-fb1e-4292-945f-867964dac1ab">ColorCorrectPalette</a> enhanced metafile record.




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




<a href="https://msdn.microsoft.com/e7680521-fb1e-4292-945f-867964dac1ab">ColorCorrectPalette</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

