---
UID: NS:wingdi.tagEMRCREATEPALETTE
title: EMRCREATEPALETTE (wingdi.h)
author: windows-sdk-content
description: The EMRCREATEPALETTE structure contains members for the CreatePalette enhanced metafile record.
old-location: gdi\emrcreatepalette.htm
tech.root: gdi
ms.assetid: 5198dc94-49bf-4cc8-8b41-2f29acd3c17d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PEMRCREATEPALETTE, EMRCREATEPALETTE, EMRCREATEPALETTE structure [Windows GDI], PEMRCREATEPALETTE, PEMRCREATEPALETTE structure pointer [Windows GDI], _win32_EMRCREATEPALETTE_str, gdi.emrcreatepalette, wingdi/EMRCREATEPALETTE, wingdi/PEMRCREATEPALETTE"
ms.topic: struct
f1_keywords: ["wingdi/EMRCREATEPALETTE"]
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
 - EMRCREATEPALETTE
product: Windows
targetos: Windows
req.typenames: EMRCREATEPALETTE, *PEMRCREATEPALETTE
req.redist: 
ms.custom: 19H1
---

# EMRCREATEPALETTE structure


## -description



The <b>EMRCREATEPALETTE</b> structure contains members for the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-createpalette">CreatePalette</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field ihPal

Index of palette in handle table.


### -field lgpl

A <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-taglogpalette">LOGPALETTE</a> structure that contains information about the palette. Note that <b>peFlags</b> members in the <a href="https://docs.microsoft.com/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a> structures do not contain any flags.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-createpalette">CreatePalette</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-taglogpalette">LOGPALETTE</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="https://docs.microsoft.com/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a>
 

 

