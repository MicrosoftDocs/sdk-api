---
UID: NS:winddi._CIECHROMA
title: CIECHROMA (winddi.h)
description: The CIECHROMA structure is used to describe the chromaticity coordinates, x and y, and the luminance, Y in CIE color space.
helpviewer_keywords: ["CIECHROMA","CIECHROMA structure [Display Devices]","display.ciechroma","grstrcts_b0ffd3e4-c5c0-40f8-9272-1decae47108d.xml","winddi/CIECHROMA"]
old-location: display\ciechroma.htm
tech.root: display
ms.assetid: b8d1fd9b-c735-49f6-8d3b-12b5b1d92543
ms.date: 12/05/2018
ms.keywords: CIECHROMA, CIECHROMA structure [Display Devices], display.ciechroma, grstrcts_b0ffd3e4-c5c0-40f8-9272-1decae47108d.xml, winddi/CIECHROMA
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: CIECHROMA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CIECHROMA
 - winddi/_CIECHROMA
 - CIECHROMA
 - winddi/CIECHROMA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - CIECHROMA
---

# CIECHROMA structure


## -description

The CIECHROMA structure is used to describe the chromaticity coordinates, <b>x</b> and <b>y</b>, and the luminance, <b>Y</b> in CIE color space.

## -struct-fields

### -field x

Specifies the x-coordinate in CIE chromaticity space.

### -field y

Specifies the y-coordinate in CIE chromaticity space.

### -field Y

Specifies the luminance. For more information, see the following Remarks section.

## -remarks

The CIECHROMA structure is used by the <a href="/windows/desktop/api/winddi/ns-winddi-colorinfo">COLORINFO</a> structure to define colors for <a href="/windows/desktop/api/winddi/ns-winddi-gdiinfo">GDIINFO</a>.

The LDECI4 type is used to represent real numbers to four decimal places. For example, (LDECI4) 10000 represents the real number 1.0000, and (LDECI4) -12345 represents -1.2345.

The values of the <b>x</b> and <b>y</b> members of CIECHROMA should be in the range from 0 through 10000--that is, the values should represent the numbers 0.0000 through 1.0000. 

The value of the <b>Y</b> member of this structure should be in the range from 0 through 100. This member can also be 65534 (0xFFFE) under certain circumstances. For more information about these circumstances, see <a href="/windows/desktop/api/winddi/ns-winddi-colorinfo">COLORINFO</a>.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-colorinfo">COLORINFO</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/ns-winddi-gdiinfo">GDIINFO</a>