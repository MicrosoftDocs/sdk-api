---
UID: NE:d2d1effects_2.D2D1_HDRTONEMAP_DISPLAY_MODE
title: D2D1_HDRTONEMAP_DISPLAY_MODE (d2d1effects_2.h)
author: windows-sdk-content
description: Defines constants that specify a value for the D2D1_HDRTONEMAP_PROP_DISPLAY_MODE property of the HDR Tone Map effect.
old-location: direct2d\d2d1_hdrtonemap_display_mode.htm
tech.root: Direct2D
ms.author: windowssdkdev
ms.date: 01/30/2019
ms.keywords: D2D1_HDRTONEMAP_DISPLAY_MODE, D2D1_HDRTONEMAP_DISPLAY_MODE enumeration [Direct2D], D2D1_HDRTONEMAP_DISPLAY_MODE_SDR, D2D1_HDRTONEMAP_DISPLAY_MODE_HDR, d2d1effects_2/D2D1_HDRTONEMAP_DISPLAY_MODE, d2d1effects_2/D2D1_HDRTONEMAP_DISPLAY_MODE_SDR, d2d1effects_2/D2D1_HDRTONEMAP_DISPLAY_MODE_HDR, direct2d.d2d1_hdrtonemap_display_mode
ms.topic: enum
f1_keywords: ["d2d1effects_2/D2D1_HDRTONEMAP_DISPLAY_MODE"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects_2.h
api_name:
 - D2D1_HDRTONEMAP_DISPLAY_MODE
product: Windows
targetos: Windows
req.typenames: D2D1_HDRTONEMAP_DISPLAY_MODE
req.redist: 
---

# D2D1_HDRTONEMAP_DISPLAY_MODE enumeration

## -description

Defines constants that specify a value for the [D2D1_HDRTONEMAP_PROP_DISPLAY_MODE](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop) property of the [HDR tone map effect](/windows/desktop/Direct2D/hdr-tone-map-effect).

## -enum-fields

### -field D2D1_HDRTONEMAP_DISPLAY_MODE_SDR (0)

Specifies that the tone mapper algorithm be optimized for best appearance on a standard dynamic range (SDR) display.

### -field D2D1_HDRTONEMAP_DISPLAY_MODE_HDR (1)

Specifies that the tone mapper algorithm be optimized for best appearance on a high dynamic range (HDR) display.

### -field D2D1_HDRTONEMAP_DISPLAY_MODE_FORCE_DWORD (0xFFFFFFFF)
