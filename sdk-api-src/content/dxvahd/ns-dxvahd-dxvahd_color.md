---
UID: NS:dxvahd._DXVAHD_COLOR
title: DXVAHD_COLOR
ms.date: 10/20/2021
targetos: Windows
description: Defines a color value for DXVA-HD.
helpviewer_keywords: ["DXVAHD_COLOR", "dxvahd/DXVAHD_COLOR"]
tech.root: mf
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: dxvahd.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: DXVAHD_COLOR
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - _DXVAHD_COLOR
 - DXVAHD_COLOR
f1_keywords:
 - _DXVAHD_COLOR
 - dxvahd/_DXVAHD_COLOR
 - DXVAHD_COLOR
 - dxvahd/DXVAHD_COLOR
dev_langs:
 - c++
---

## -description

Defines a color value for DXVA-HD.

## -struct-fields

### -field RGB

A [DXVAHD_COLOR_RGBA](./ns-dxvahd-dxvahd_color_rgba.md) structure that contains an RGB color value.

### -field YCbCr

A [DXVAHD_COLOR_YCbCrA](./ns-dxvahd-dxvahd_color_ycbcra.md) structure that contains a YCbCr color value.

## -remarks

This union can represent both RGB and YCbCr colors. The interpretation of the union depends on the context.

## -see-also
