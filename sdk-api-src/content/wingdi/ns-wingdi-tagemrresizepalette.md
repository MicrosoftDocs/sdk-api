---
UID: NS:wingdi.tagEMRRESIZEPALETTE
title: tagEMRRESIZEPALETTE
author: windows-sdk-content
description: The EMRRESIZEPALETTE structure contains members for the ResizePalette enhanced metafile record.
old-location: gdi\emrresizepalette.htm
tech.root: gdi
ms.assetid: b9c31591-bf9f-44d9-8c9a-9682d29fc541
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PEMRRESIZEPALETTE, EMRRESIZEPALETTE, EMRRESIZEPALETTE structure [Windows GDI], PEMRRESIZEPALETTE, PEMRRESIZEPALETTE structure pointer [Windows GDI], _win32_EMRRESIZEPALETTE_str, gdi.emrresizepalette, tagEMRRESIZEPALETTE, wingdi/EMRRESIZEPALETTE, wingdi/PEMRRESIZEPALETTE"
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
 - EMRRESIZEPALETTE
product: Windows
targetos: Windows
req.typenames: EMRRESIZEPALETTE, *PEMRRESIZEPALETTE
req.redist: 
---

# tagEMRRESIZEPALETTE structure


## -description



The <b>EMRRESIZEPALETTE</b> structure contains members for the <b>ResizePalette</b> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field ihPal

Index of the palette in the handle table.


### -field cEntries

Number of entries in palette after resizing.


## -see-also




<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/77178869-cbfb-4b91-a5b0-7d0404e7534f">ResizePalette</a>
 

 

