---
UID: NS:wingdi.tagPALETTEENTRY
title: PALETTEENTRY (wingdi.h)
description: Specifies the color and usage of an entry in a logical palette.
helpviewer_keywords: ["*LPPALETTEENTRY","*PPALETTEENTRY","523c466d-5003-02e3-c336-f0e36539855e","LPPALETTEENTRY","LPPALETTEENTRY structure pointer [Direct3D 9]","PALETTEENTRY","PALETTEENTRY structure [Direct3D 9]","direct3d9.paletteentry","wingdi/LPPALETTEENTRY","wingdi/PALETTEENTRY"]
old-location: direct3d9\paletteentry.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\paletteentry.htm
ms.date: 12/05/2024
ms.keywords: '*LPPALETTEENTRY, *PPALETTEENTRY, 523c466d-5003-02e3-c336-f0e36539855e, LPPALETTEENTRY, LPPALETTEENTRY structure pointer [Direct3D 9], PALETTEENTRY, PALETTEENTRY structure [Direct3D 9], direct3d9.paletteentry, wingdi/LPPALETTEENTRY, wingdi/PALETTEENTRY'
req.header: wingdi.h
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
req.typenames: PALETTEENTRY, *PPALETTEENTRY, *LPPALETTEENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPALETTEENTRY
 - wingdi/tagPALETTEENTRY
 - PPALETTEENTRY
 - wingdi/PPALETTEENTRY
 - PALETTEENTRY
 - wingdi/PALETTEENTRY
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
 - PALETTEENTRY
---

## -description

Specifies the color and usage of an entry in a logical palette. In GDI, a logical palette is defined by a [LOGPALETTE](/windows/win32/api/wingdi/ns-wingdi-logpalette) structure. In Direct3D, logical palettes are used in a [D3DHAL_DP2UPDATEPALETTE](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_dp2updatepalette) structure.

## -struct-fields

### -field peRed

Type: **[BYTE](/windows/win32/winprog/windows-data-types)**

The red intensity value for the palette entry.

### -field peGreen

Type: **[BYTE](/windows/win32/winprog/windows-data-types)**

The green intensity value for the palette entry.

### -field peBlue

Type: **[BYTE](/windows/win32/winprog/windows-data-types)**

The blue intensity value for the palette entry.

### -field peFlags

Type: **[BYTE](/windows/win32/winprog/windows-data-types)**

For the GDI use case of logical palettes, *peFlags* indicates how the palette entry is to be used. This member may be set to zero or one of the following values.

|Value|Meaning|
|-|-|
|**PC_EXPLICIT**|Specifies that the low-order word of the logical palette entry designates a hardware palette index. This flag allows the application to show the contents of the display device palette.|
|**PC_NOCOLLAPSE**|Specifies that the color be placed in an unused entry in the system palette instead of being matched to an existing color in the system palette. If there are no unused entries in the system palette, the color is matched normally. Once this color is in the system palette, colors in other logical palettes can be matched to this color.|
|**PC_RESERVED**|Specifies that the logical palette entry be used for palette animation. This flag prevents other windows from matching colors to the palette entry since the color frequently changes. If an unused system-palette entry is available, the color is placed in that entry. Otherwise, the color is not available for animation.|

For the Direct3D use case of logical palettes, *peFlags* represents the alpha intensity value for the palette entry..

## -see-also

* [Direct3D structures](/windows/win32/direct3d9/dx9-graphics-reference-d3d-structures)
