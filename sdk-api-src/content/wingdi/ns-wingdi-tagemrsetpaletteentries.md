---
UID: NS:wingdi.tagEMRSETPALETTEENTRIES
title: tagEMRSETPALETTEENTRIES
author: windows-sdk-content
description: The EMRSETPALETTEENTRIES structure contains members for the SetPaletteEntries enhanced metafile record.
old-location: gdi\emrsetpaletteentries.htm
tech.root: gdi
ms.assetid: df75567e-150f-4f88-b6ae-938b451a7b7d
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PEMRSETPALETTEENTRIES, EMRSETPALETTEENTRIES, EMRSETPALETTEENTRIES structure [Windows GDI], PEMRSETPALETTEENTRIES, PEMRSETPALETTEENTRIES structure pointer [Windows GDI], _win32_EMRSETPALETTEENTRIES_str, gdi.emrsetpaletteentries, tagEMRSETPALETTEENTRIES, wingdi/EMRSETPALETTEENTRIES, wingdi/PEMRSETPALETTEENTRIES"
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
 - EMRSETPALETTEENTRIES
product: Windows
targetos: Windows
req.typenames: EMRSETPALETTEENTRIES, *PEMRSETPALETTEENTRIES
req.redist: 
---

# tagEMRSETPALETTEENTRIES structure


## -description



The <b>EMRSETPALETTEENTRIES</b> structure contains members for the <a href="https://msdn.microsoft.com/df38f482-75ba-4800-8b26-92204c63255e">SetPaletteEntries</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field ihPal

Palette handle index.


### -field iStart

Index of first entry to set.


### -field cEntries

Number of entries.


### -field aPalEntries

Array of <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structures. Note that <b>peFlags</b> members in the structures do not contain any flags.


## -see-also




<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a>



<a href="https://msdn.microsoft.com/df38f482-75ba-4800-8b26-92204c63255e">SetPaletteEntries</a>
 

 

