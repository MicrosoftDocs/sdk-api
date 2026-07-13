---
UID: NE:d2d1effects_2.D2D1_HDRTONEMAP_PROP
title: D2D1_HDRTONEMAP_PROP (d2d1effects_2.h)
description: Defines constants that identify the top level properties of the HDR Tone Map effect.
helpviewer_keywords: ["D2D1_HDRTONEMAP_PROP","D2D1_HDRTONEMAP_PROP enumeration [Direct2D]","D2D1_HDRTONEMAP_PROP_INPUT_MAX_LUMINANCE","D2D1_HDRTONEMAP_PROP_OUTPUT_MAX_LUMINANCE","D2D1_HDRTONEMAP_PROP_DISPLAY_MODE","d2d1effects_2/D2D1_HDRTONEMAP_PROP","d2d1effects_2/D2D1_HDRTONEMAP_PROP_INPUT_MAX_LUMINANCE","d2d1effects_2/D2D1_HDRTONEMAP_PROP_OUTPUT_MAX_LUMINANCE","d2d1effects_2/D2D1_HDRTONEMAP_PROP_DISPLAY_MODE","direct2d.d2d1_hdrtonemap_prop"]
old-location: direct2d\d2d1_hdrtonemap_prop.htm
tech.root: Direct2D
ms.date: 01/30/2019
ms.keywords: D2D1_HDRTONEMAP_PROP, D2D1_HDRTONEMAP_PROP enumeration [Direct2D], D2D1_HDRTONEMAP_PROP_INPUT_MAX_LUMINANCE, D2D1_HDRTONEMAP_PROP_OUTPUT_MAX_LUMINANCE, D2D1_HDRTONEMAP_PROP_DISPLAY_MODE, d2d1effects_2/D2D1_HDRTONEMAP_PROP, d2d1effects_2/D2D1_HDRTONEMAP_PROP_INPUT_MAX_LUMINANCE, d2d1effects_2/D2D1_HDRTONEMAP_PROP_OUTPUT_MAX_LUMINANCE, d2d1effects_2/D2D1_HDRTONEMAP_PROP_DISPLAY_MODE, direct2d.d2d1_hdrtonemap_prop
req.header: d2d1effects_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
req.typenames: D2D1_HDRTONEMAP_PROP
req.redist: 
f1_keywords:
 - D2D1_HDRTONEMAP_PROP
 - d2d1effects_2/D2D1_HDRTONEMAP_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects_2.h
api_name:
 - D2D1_HDRTONEMAP_PROP
---

# D2D1_HDRTONEMAP_PROP enumeration


## -description

Defines constants that identify the top level properties of the [HDR tone map effect](/windows/desktop/Direct2D/hdr-tone-map-effect). The effect adjusts the maximum luminance of the source image to fit within the maximum output luminance supported. Input and output luminance values are specified in nits. Note that the color space of the target image is assumed to be scRGB.

## -enum-fields

### -field D2D1_HDRTONEMAP_PROP_INPUT_MAX_LUMINANCE (0)

Identifies the `InputMaxLuminance` property of the effect. The property is of type FLOAT, and is specified in nits.

### -field D2D1_HDRTONEMAP_PROP_OUTPUT_MAX_LUMINANCE (1)

Identifies the `OutputMaxLuminance` property of the effect. The property is of type FLOAT, and is specified in nits.

### -field D2D1_HDRTONEMAP_PROP_DISPLAY_MODE (2)

Identifies the `DisplayMode` property of the effect. The property is of type <a href="/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_display_mode"><strong>D2D1_HDRTONEMAP_DISPLAY_MODE</strong></a>.

### -field D2D1_HDRTONEMAP_PROP_FORCE_DWORD (0xFFFFFFFF)
