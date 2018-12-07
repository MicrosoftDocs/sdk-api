---
UID: NS:wingdi.tagEMRCREATEPALETTE
title: tagEMRCREATEPALETTE
author: windows-sdk-content
description: The EMRCREATEPALETTE structure contains members for the CreatePalette enhanced metafile record.
old-location: gdi\emrcreatepalette.htm
tech.root: gdi
ms.assetid: 5198dc94-49bf-4cc8-8b41-2f29acd3c17d
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PEMRCREATEPALETTE, EMRCREATEPALETTE, EMRCREATEPALETTE structure [Windows GDI], PEMRCREATEPALETTE, PEMRCREATEPALETTE structure pointer [Windows GDI], _win32_EMRCREATEPALETTE_str, gdi.emrcreatepalette, tagEMRCREATEPALETTE, wingdi/EMRCREATEPALETTE, wingdi/PEMRCREATEPALETTE"
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
 - EMRCREATEPALETTE
product: Windows
targetos: Windows
req.typenames: EMRCREATEPALETTE, *PEMRCREATEPALETTE
req.redist: 
---

# tagEMRCREATEPALETTE structure


## -description



The <b>EMRCREATEPALETTE</b> structure contains members for the <a href="https://msdn.microsoft.com/f3462198-9360-4b77-ac62-9fe21ec666be">CreatePalette</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field ihPal

Index of palette in handle table.


### -field lgpl

A <a href="https://msdn.microsoft.com/99d70a0e-ac61-4a88-a500-66443e7882ad">LOGPALETTE</a> structure that contains information about the palette. Note that <b>peFlags</b> members in the <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structures do not contain any flags.


## -see-also




<a href="https://msdn.microsoft.com/f3462198-9360-4b77-ac62-9fe21ec666be">CreatePalette</a>



<a href="https://msdn.microsoft.com/99d70a0e-ac61-4a88-a500-66443e7882ad">LOGPALETTE</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a>
 

 

