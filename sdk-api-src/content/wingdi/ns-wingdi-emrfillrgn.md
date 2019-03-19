---
UID: NS:wingdi.tagEMRFILLRGN
title: EMRFILLRGN (wingdi.h)
author: windows-sdk-content
description: The EMRFILLRGN structure contains members for the FillRgn enhanced metafile record.
old-location: gdi\emrfillrgn.htm
tech.root: gdi
ms.assetid: 84b81b9d-3def-403c-94cd-8f5ddea02d6d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PEMRFILLRGN, EMRFILLRGN, EMRFILLRGN structure [Windows GDI], PEMRFILLRGN, PEMRFILLRGN structure pointer [Windows GDI], _win32_EMRFILLRGN_str, gdi.emrfillrgn, wingdi/EMRFILLRGN, wingdi/PEMRFILLRGN"
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
 - EMRFILLRGN
product: Windows
targetos: Windows
req.typenames: EMRFILLRGN, *PEMRFILLRGN
req.redist: 
---

# EMRFILLRGN structure


## -description



The <b>EMRFILLRGN</b> structure contains members for the <a href="https://msdn.microsoft.com/c4e0eca5-442b-462b-a4f2-0c628b6d3d38">FillRgn</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field rclBounds

Bounding rectangle, in device units.


### -field cbRgnData

Size of region data, in bytes.


### -field ihBrush

Index of brush, in handle table.


### -field RgnData

Buffer containing <a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/c4e0eca5-442b-462b-a4f2-0c628b6d3d38">FillRgn</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a>
 

 

