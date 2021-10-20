---
UID: NS:mfobjects._MFPaletteEntry
title: MFPaletteEntry
ms.date: 10/16/2020
targetos: Windows
helpviewer_keywords: ["MFPaletteEntry","mfobjects/MFPaletteEntry"]
description: Contains one palette entry in a color table.
tech.root: mf
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: mfobjects.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: MFPaletteEntry
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - _MFPaletteEntry
 - MFPaletteEntry
f1_keywords:
 - _MFPaletteEntry
 - mfobjects/_MFPaletteEntry
 - MFPaletteEntry
 - mfobjects/MFPaletteEntry
dev_langs:
 - c++
---

## -description

Contains one palette entry in a color table.

## -struct-fields

### -field ARGB

[MFARGB](./ns-mfobjects-mfargb.md) structure that contains an RGB color.

### -field AYCbCr

[MFAYUVSample](./ns-mfobjects-mfayuvsample.md) structure that contains a Y'Cb'Cr' color.

## -remarks

This union can be used to represent both RGB palettes and Y'Cb'Cr' palettes. The video format that defines the palette determines which union member should be used.
     

## -see-also
