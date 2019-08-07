---
UID: NS:wingdi.tagEMRFRAMERGN
title: EMRFRAMERGN (wingdi.h)
author: windows-sdk-content
description: The EMRFRAMERGN structure contains members for the FrameRgn enhanced metafile record.
old-location: gdi\emrframergn.htm
tech.root: gdi
ms.assetid: 578a2824-b42e-401d-b4b0-8426440713c6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PEMRFRAMERGN, EMRFRAMERGN, EMRFRAMERGN structure [Windows GDI], PEMRFRAMERGN, PEMRFRAMERGN structure pointer [Windows GDI], _win32_EMRFRAMERGN_str, gdi.emrframergn, wingdi/EMRFRAMERGN, wingdi/PEMRFRAMERGN'
ms.topic: struct
f1_keywords:
- wingdi/EMRFRAMERGN
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
- EMRFRAMERGN
product: Windows
targetos: Windows
req.typenames: EMRFRAMERGN, *PEMRFRAMERGN
req.redist: 
ms.custom: 19H1
---

# EMRFRAMERGN structure


## -description



The <b>EMRFRAMERGN</b> structure contains members for the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-framergn">FrameRgn</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field rclBounds

Bounding rectangle, in device units.


### -field cbRgnData

Size of region data, in bytes.


### -field ihBrush

Index of brush, in handle table.


### -field szlStroke

Width and height of region frame, in logical units.


### -field RgnData

Buffer containing <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-rgndata">RGNDATA</a> structure.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-framergn">FrameRgn</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-rgndata">RGNDATA</a>
 

 

