---
UID: NE:wincodec.WICBitmapPaletteType
title: WICBitmapPaletteType (wincodec.h)
description: Specifies the type of palette used for an indexed image format.
helpviewer_keywords: ["WICBitmapPaletteType","WICBitmapPaletteType enumeration [Windows Imaging Component]","WICBitmapPaletteTypeCustom","WICBitmapPaletteTypeFixedBW","WICBitmapPaletteTypeFixedGray16","WICBitmapPaletteTypeFixedGray256","WICBitmapPaletteTypeFixedGray4","WICBitmapPaletteTypeFixedHalftone125","WICBitmapPaletteTypeFixedHalftone216","WICBitmapPaletteTypeFixedHalftone252","WICBitmapPaletteTypeFixedHalftone256","WICBitmapPaletteTypeFixedHalftone27","WICBitmapPaletteTypeFixedHalftone64","WICBitmapPaletteTypeFixedHalftone8","WICBitmapPaletteTypeFixedWebPalette","WICBitmapPaletteTypeMedianCut","_wic_codec_wicbitmappalettetype","wic._wic_codec_wicbitmappalettetype","wincodec/WICBitmapPaletteType","wincodec/WICBitmapPaletteTypeCustom","wincodec/WICBitmapPaletteTypeFixedBW","wincodec/WICBitmapPaletteTypeFixedGray16","wincodec/WICBitmapPaletteTypeFixedGray256","wincodec/WICBitmapPaletteTypeFixedGray4","wincodec/WICBitmapPaletteTypeFixedHalftone125","wincodec/WICBitmapPaletteTypeFixedHalftone216","wincodec/WICBitmapPaletteTypeFixedHalftone252","wincodec/WICBitmapPaletteTypeFixedHalftone256","wincodec/WICBitmapPaletteTypeFixedHalftone27","wincodec/WICBitmapPaletteTypeFixedHalftone64","wincodec/WICBitmapPaletteTypeFixedHalftone8","wincodec/WICBitmapPaletteTypeFixedWebPalette","wincodec/WICBitmapPaletteTypeMedianCut"]
old-location: wic\_wic_codec_wicbitmappalettetype.htm
tech.root: wic
ms.assetid: a8192905-2bae-4760-bf2d-64640c46e168
ms.date: 12/05/2018
ms.keywords: WICBitmapPaletteType, WICBitmapPaletteType enumeration [Windows Imaging Component], WICBitmapPaletteTypeCustom, WICBitmapPaletteTypeFixedBW, WICBitmapPaletteTypeFixedGray16, WICBitmapPaletteTypeFixedGray256, WICBitmapPaletteTypeFixedGray4, WICBitmapPaletteTypeFixedHalftone125, WICBitmapPaletteTypeFixedHalftone216, WICBitmapPaletteTypeFixedHalftone252, WICBitmapPaletteTypeFixedHalftone256, WICBitmapPaletteTypeFixedHalftone27, WICBitmapPaletteTypeFixedHalftone64, WICBitmapPaletteTypeFixedHalftone8, WICBitmapPaletteTypeFixedWebPalette, WICBitmapPaletteTypeMedianCut, _wic_codec_wicbitmappalettetype, wic._wic_codec_wicbitmappalettetype, wincodec/WICBitmapPaletteType, wincodec/WICBitmapPaletteTypeCustom, wincodec/WICBitmapPaletteTypeFixedBW, wincodec/WICBitmapPaletteTypeFixedGray16, wincodec/WICBitmapPaletteTypeFixedGray256, wincodec/WICBitmapPaletteTypeFixedGray4, wincodec/WICBitmapPaletteTypeFixedHalftone125, wincodec/WICBitmapPaletteTypeFixedHalftone216, wincodec/WICBitmapPaletteTypeFixedHalftone252, wincodec/WICBitmapPaletteTypeFixedHalftone256, wincodec/WICBitmapPaletteTypeFixedHalftone27, wincodec/WICBitmapPaletteTypeFixedHalftone64, wincodec/WICBitmapPaletteTypeFixedHalftone8, wincodec/WICBitmapPaletteTypeFixedWebPalette, wincodec/WICBitmapPaletteTypeMedianCut
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WICBitmapPaletteType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICBitmapPaletteType
 - wincodec/WICBitmapPaletteType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICBitmapPaletteType
---

# WICBitmapPaletteType enumeration


## -description

Specifies the type of palette used for an indexed image format.

## -enum-fields

### -field WICBitmapPaletteTypeCustom:0

An arbitrary custom palette provided by caller.

### -field WICBitmapPaletteTypeMedianCut:0x1

An optimal palette generated using a median-cut algorithm. Derived from the colors in an image.

### -field WICBitmapPaletteTypeFixedBW:0x2

A black and white palette.

### -field WICBitmapPaletteTypeFixedHalftone8:0x3

A palette that has its 8-color on-off primaries and the 16 system colors added. With duplicates removed, 16 colors are available.

### -field WICBitmapPaletteTypeFixedHalftone27:0x4

A palette that has 3 intensity levels of each primary: 27-color on-off primaries and the 16 system colors added. With duplicates removed, 35 colors are available.

### -field WICBitmapPaletteTypeFixedHalftone64:0x5

A palette that has 4 intensity levels of each primary: 64-color on-off primaries and the 16 system colors added. With duplicates removed, 72 colors are available.

### -field WICBitmapPaletteTypeFixedHalftone125:0x6

A palette that has 5 intensity levels of each primary: 125-color on-off primaries and the 16 system colors added. With duplicates removed, 133 colors are available.

### -field WICBitmapPaletteTypeFixedHalftone216:0x7

A palette that has 6 intensity levels of each primary: 216-color on-off primaries and the 16 system colors added. With duplicates removed, 224 colors are available. This is the same as <b>WICBitmapPaletteFixedHalftoneWeb</b>.

### -field WICBitmapPaletteTypeFixedWebPalette

A palette that has 6 intensity levels of each primary: 216-color on-off primaries and the 16 system colors added. With duplicates removed, 224 colors are available. This is the same as <b>WICBitmapPaletteTypeFixedHalftone216</b>.

### -field WICBitmapPaletteTypeFixedHalftone252:0x8

A palette that has its 252-color on-off primaries and the 16 system colors added. With duplicates removed, 256 colors are available.

### -field WICBitmapPaletteTypeFixedHalftone256:0x9

A palette that has its 256-color on-off primaries and the 16 system colors added. With duplicates removed, 256 colors are available.

### -field WICBitmapPaletteTypeFixedGray4:0xa

A palette that has 4 shades of gray.

### -field WICBitmapPaletteTypeFixedGray16:0xb

A palette that has 16 shades of gray.

### -field WICBitmapPaletteTypeFixedGray256:0xc

A palette that has 256 shades of gray.

### -field WICBITMAPPALETTETYPE_FORCE_DWORD:0x7fffffff

