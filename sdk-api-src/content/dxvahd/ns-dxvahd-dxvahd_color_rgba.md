---
UID: NS:dxvahd._DXVAHD_COLOR_RGBA
title: DXVAHD_COLOR_RGBA (dxvahd.h)
description: Specifies an RGB color value. (DXVAHD_COLOR_RGBA)
helpviewer_keywords: ["DXVAHD_COLOR_RGBA","DXVAHD_COLOR_RGBA structure [Media Foundation]","dxvahd/DXVAHD_COLOR_RGBA","mf.dxvahd_color_rgba"]
old-location: mf\dxvahd_color_rgba.htm
tech.root: mf
ms.assetid: 60a167cb-f95e-4eb5-995f-be4cceaee47d
ms.date: 12/05/2018
ms.keywords: DXVAHD_COLOR_RGBA, DXVAHD_COLOR_RGBA structure [Media Foundation], dxvahd/DXVAHD_COLOR_RGBA, mf.dxvahd_color_rgba
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DXVAHD_COLOR_RGBA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_COLOR_RGBA
 - dxvahd/_DXVAHD_COLOR_RGBA
 - DXVAHD_COLOR_RGBA
 - dxvahd/DXVAHD_COLOR_RGBA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_COLOR_RGBA
---

# DXVAHD_COLOR_RGBA structure


## -description

Specifies an RGB color value.

## -struct-fields

### -field R

The red value.

### -field G

The green value.

### -field B

The blue value.

### -field A

The alpha value. Values range from 0 (transparent) to 1 (opaque).

## -remarks

The RGB values have a nominal range of [0...1]. For an RGB format with  <i>n</i> bits per channel, the value of each color component is calculated as follows:

<code>val = f * ((1 &lt;&lt; n)-1)</code>

For example, for RGB-32 (8 bits per channel), <code>val = BYTE(f * 255.0)</code>.

For full-range RGB, reference black is (0.0, 0.0, 0.0), which corresponds to (0, 0, 0) in an 8-bit representation. For limited-range RGB, reference black is (0.0625, 0.0625, 0.0625), which corresponds to (16, 16, 16) in an 8-bit representation. For wide-gamut formats, the values might fall outside of the [0...1] range.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>
