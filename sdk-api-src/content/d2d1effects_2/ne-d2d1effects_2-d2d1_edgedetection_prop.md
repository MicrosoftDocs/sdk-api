---
UID: NE:d2d1effects_2.D2D1_EDGEDETECTION_PROP
title: D2D1_EDGEDETECTION_PROP (d2d1effects_2.h)
description: Identifiers for properties of the Edge Detection effect.
helpviewer_keywords: ["D2D1_EDGEDETECTION_PROP","D2D1_EDGEDETECTION_PROP enumeration [Direct2D]","D2D1_EDGEDETECTION_PROP_ALPHA_MODE","D2D1_EDGEDETECTION_PROP_BLUR_RADIUS","D2D1_EDGEDETECTION_PROP_MODE","D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES","D2D1_EDGEDETECTION_PROP_STRENGTH","d2d1effects_2/D2D1_EDGEDETECTION_PROP","d2d1effects_2/D2D1_EDGEDETECTION_PROP_ALPHA_MODE","d2d1effects_2/D2D1_EDGEDETECTION_PROP_BLUR_RADIUS","d2d1effects_2/D2D1_EDGEDETECTION_PROP_MODE","d2d1effects_2/D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES","d2d1effects_2/D2D1_EDGEDETECTION_PROP_STRENGTH","direct2d.d2d1_edgedetection_prop"]
old-location: direct2d\d2d1_edgedetection_prop.htm
tech.root: Direct2D
ms.assetid: F3B94BDC-120E-4B44-9AA8-595AAEFD1F61
ms.date: 12/05/2018
ms.keywords: D2D1_EDGEDETECTION_PROP, D2D1_EDGEDETECTION_PROP enumeration [Direct2D], D2D1_EDGEDETECTION_PROP_ALPHA_MODE, D2D1_EDGEDETECTION_PROP_BLUR_RADIUS, D2D1_EDGEDETECTION_PROP_MODE, D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES, D2D1_EDGEDETECTION_PROP_STRENGTH, d2d1effects_2/D2D1_EDGEDETECTION_PROP, d2d1effects_2/D2D1_EDGEDETECTION_PROP_ALPHA_MODE, d2d1effects_2/D2D1_EDGEDETECTION_PROP_BLUR_RADIUS, d2d1effects_2/D2D1_EDGEDETECTION_PROP_MODE, d2d1effects_2/D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES, d2d1effects_2/D2D1_EDGEDETECTION_PROP_STRENGTH, direct2d.d2d1_edgedetection_prop
req.header: d2d1effects_2.h
req.include-header: 
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
req.typenames: D2D1_EDGEDETECTION_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_EDGEDETECTION_PROP
 - d2d1effects_2/D2D1_EDGEDETECTION_PROP
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
 - D2D1_EDGEDETECTION_PROP
---

# D2D1_EDGEDETECTION_PROP enumeration


## -description

Identifiers for properties of the Edge Detection effect.

## -enum-fields

### -field D2D1_EDGEDETECTION_PROP_STRENGTH:0

The D2D1_EDGEDETECTION_PROP_STRENGTH property is a float value modulating the response of the edge detection filter. A low strength value means that weaker edges will get filtered out, 
          while a high value means stronger edges will get filtered out.  The allowed range is 0.0 to 1.0.  The default value is 0.5.

### -field D2D1_EDGEDETECTION_PROP_BLUR_RADIUS:1

The D2D1_EDGEDETECTION_PROP_BLUR_RADIUS property is a float value specifying the amount of blur to apply.  Applying blur is used to remove high frequencies and reduce phantom edges.  
          The allowed range is 0.0 to 10.0. The default value is 0.0 (no blur applied).

### -field D2D1_EDGEDETECTION_PROP_MODE:2

The D2D1_EDGEDETECTION_PROP_MODE property is a <a href="/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_mode">D2D1_EDGEDETECTION_MODE</a> enumeration value which mode to use for edge detection.  
          The default value is D2D1_EDGEDETECTION_MODE_SOBEL.

### -field D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES:3

The D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES property is a boolean value. Edge detection only applies to the RGB channels, the alpha channel is ignored for purposes of detecting edges.
          If D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES is false, the output edges is fully opaque. If D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES is true, the input opacity is preserved.
          The default value is false.

### -field D2D1_EDGEDETECTION_PROP_ALPHA_MODE:4

The D2D1_EDGEDETECTION_PROP_ALPHA_MODE property is a <a href="/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE</a> enumeration value indicating the alpha mode of the input file.
          If the input is not opaque, this value is used to determine whether to unpremultiply the inputs.
          See the About Alpha Modes section of the <a href="/windows/desktop/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a> topic for additional information.   
          
          The default value is D2D1_ALPHA_MODE_PREMULTIPLIED.

### -field D2D1_EDGEDETECTION_PROP_FORCE_DWORD:0xffffffff
