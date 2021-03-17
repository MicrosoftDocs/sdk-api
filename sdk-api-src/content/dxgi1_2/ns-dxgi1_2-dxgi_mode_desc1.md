---
UID: NS:dxgi1_2.DXGI_MODE_DESC1
title: DXGI_MODE_DESC1 (dxgi1_2.h)
description: Describes a display mode and whether the display mode supports stereo.
helpviewer_keywords: ["DXGI_MODE_DESC1","DXGI_MODE_DESC1 structure [DXGI]","direct3ddxgi.dxgi_mode_desc1","dxgi1_2/DXGI_MODE_DESC1"]
old-location: direct3ddxgi\dxgi_mode_desc1.htm
tech.root: direct3ddxgi
ms.assetid: 8F44CF77-D3A1-44F7-AB7F-69E5727A4378
ms.date: 12/05/2018
ms.keywords: DXGI_MODE_DESC1, DXGI_MODE_DESC1 structure [DXGI], direct3ddxgi.dxgi_mode_desc1, dxgi1_2/DXGI_MODE_DESC1
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: DXGI_MODE_DESC1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_MODE_DESC1
 - dxgi1_2/DXGI_MODE_DESC1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_2.h
api_name:
 - DXGI_MODE_DESC1
---

# DXGI_MODE_DESC1 structure


## -description

Describes a display mode and whether the display mode supports stereo.

## -struct-fields

### -field Width

A value that describes the resolution width.

### -field Height

A value that describes the resolution height.

### -field RefreshRate

A <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational">DXGI_RATIONAL</a> structure that describes the refresh rate in hertz.

### -field Format

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value that describes the display format.

### -field ScanlineOrdering

A <a href="/previous-versions/windows/desktop/legacy/bb173067(v=vs.85)">DXGI_MODE_SCANLINE_ORDER</a>-typed value that describes the scan-line drawing mode.

### -field Scaling

A <a href="/previous-versions/windows/desktop/legacy/bb173066(v=vs.85)">DXGI_MODE_SCALING</a>-typed value that describes the scaling mode.

### -field Stereo

Specifies whether the full-screen display mode is stereo. <b>TRUE</b> if stereo; otherwise, <b>FALSE</b>.

## -remarks

<b>DXGI_MODE_DESC1</b> is identical to <a href="/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)">DXGI_MODE_DESC</a> except that <b>DXGI_MODE_DESC1</b> includes the <b>Stereo</b> member.

This structure is used by the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1">GetDisplayModeList1</a> and <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1">FindClosestMatchingMode1</a> methods.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>