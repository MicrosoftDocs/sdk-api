---
UID: NS:wingdi._RGNDATAHEADER
title: RGNDATAHEADER (wingdi.h)
description: The RGNDATAHEADER structure describes the data returned by the GetRegionData function.
helpviewer_keywords: ["*PRGNDATAHEADER","PRGNDATAHEADER","PRGNDATAHEADER structure pointer [Windows GDI]","RGNDATAHEADER","RGNDATAHEADER structure [Windows GDI]","_RGNDATAHEADER","_win32_RGNDATAHEADER_str","gdi.rgndataheader","wingdi/PRGNDATAHEADER","wingdi/RGNDATAHEADER"]
old-location: gdi\rgndataheader.htm
tech.root: gdi
ms.assetid: 15990903-8a48-4c47-b527-269d775255a5
ms.date: 12/05/2018
ms.keywords: '*PRGNDATAHEADER, PRGNDATAHEADER, PRGNDATAHEADER structure pointer [Windows GDI], RGNDATAHEADER, RGNDATAHEADER structure [Windows GDI], _RGNDATAHEADER, _win32_RGNDATAHEADER_str, gdi.rgndataheader, wingdi/PRGNDATAHEADER, wingdi/RGNDATAHEADER'
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
targetos: Windows
req.typenames: RGNDATAHEADER, *PRGNDATAHEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RGNDATAHEADER
 - wingdi/_RGNDATAHEADER
 - PRGNDATAHEADER
 - wingdi/PRGNDATAHEADER
 - RGNDATAHEADER
 - wingdi/RGNDATAHEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - RGNDATAHEADER
---

# RGNDATAHEADER structure


## -description

The <b>RGNDATAHEADER</b> structure describes the data returned by the <a href="/windows/desktop/api/wingdi/nf-wingdi-getregiondata">GetRegionData</a> function.

## -struct-fields

### -field dwSize

The size, in bytes, of the header.

### -field iType

The type of region. This value must be RDH_RECTANGLES.

### -field nCount

The number of rectangles that make up the region.

### -field nRgnSize

The size of the <a href="/windows/desktop/api/wingdi/ns-wingdi-rgndata">RGNDATA</a> buffer required to receive the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structures that make up the region. If the size is not known, this member can be zero.

### -field rcBound

A bounding rectangle for the region in logical units.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-getregiondata">GetRegionData</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-rgndata">RGNDATA</a>



<a href="/windows/desktop/gdi/region-structures">Region Structures</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>