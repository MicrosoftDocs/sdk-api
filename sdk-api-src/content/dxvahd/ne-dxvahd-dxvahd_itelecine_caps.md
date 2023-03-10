---
UID: NE:dxvahd._DXVAHD_ITELECINE_CAPS
title: DXVAHD_ITELECINE_CAPS (dxvahd.h)
description: Specifies the inverse telecine (IVTC) capabilities of a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
helpviewer_keywords: ["DXVAHD_ITELECINE_CAPS","DXVAHD_ITELECINE_CAPS enumeration [Media Foundation]","DXVAHD_ITELECINE_CAPS_22","DXVAHD_ITELECINE_CAPS_222222222223","DXVAHD_ITELECINE_CAPS_2224","DXVAHD_ITELECINE_CAPS_2332","DXVAHD_ITELECINE_CAPS_32","DXVAHD_ITELECINE_CAPS_32322","DXVAHD_ITELECINE_CAPS_55","DXVAHD_ITELECINE_CAPS_64","DXVAHD_ITELECINE_CAPS_87","DXVAHD_ITELECINE_CAPS_OTHER","dxvahd/DXVAHD_ITELECINE_CAPS","dxvahd/DXVAHD_ITELECINE_CAPS_22","dxvahd/DXVAHD_ITELECINE_CAPS_222222222223","dxvahd/DXVAHD_ITELECINE_CAPS_2224","dxvahd/DXVAHD_ITELECINE_CAPS_2332","dxvahd/DXVAHD_ITELECINE_CAPS_32","dxvahd/DXVAHD_ITELECINE_CAPS_32322","dxvahd/DXVAHD_ITELECINE_CAPS_55","dxvahd/DXVAHD_ITELECINE_CAPS_64","dxvahd/DXVAHD_ITELECINE_CAPS_87","dxvahd/DXVAHD_ITELECINE_CAPS_OTHER","mf.dxvahd_itelecine_caps"]
old-location: mf\dxvahd_itelecine_caps.htm
tech.root: mf
ms.assetid: bf3e0d24-2671-4e79-9cfe-d776d8e5fb47
ms.date: 12/05/2018
ms.keywords: DXVAHD_ITELECINE_CAPS, DXVAHD_ITELECINE_CAPS enumeration [Media Foundation], DXVAHD_ITELECINE_CAPS_22, DXVAHD_ITELECINE_CAPS_222222222223, DXVAHD_ITELECINE_CAPS_2224, DXVAHD_ITELECINE_CAPS_2332, DXVAHD_ITELECINE_CAPS_32, DXVAHD_ITELECINE_CAPS_32322, DXVAHD_ITELECINE_CAPS_55, DXVAHD_ITELECINE_CAPS_64, DXVAHD_ITELECINE_CAPS_87, DXVAHD_ITELECINE_CAPS_OTHER, dxvahd/DXVAHD_ITELECINE_CAPS, dxvahd/DXVAHD_ITELECINE_CAPS_22, dxvahd/DXVAHD_ITELECINE_CAPS_222222222223, dxvahd/DXVAHD_ITELECINE_CAPS_2224, dxvahd/DXVAHD_ITELECINE_CAPS_2332, dxvahd/DXVAHD_ITELECINE_CAPS_32, dxvahd/DXVAHD_ITELECINE_CAPS_32322, dxvahd/DXVAHD_ITELECINE_CAPS_55, dxvahd/DXVAHD_ITELECINE_CAPS_64, dxvahd/DXVAHD_ITELECINE_CAPS_87, dxvahd/DXVAHD_ITELECINE_CAPS_OTHER, mf.dxvahd_itelecine_caps
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
req.typenames: DXVAHD_ITELECINE_CAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_ITELECINE_CAPS
 - dxvahd/_DXVAHD_ITELECINE_CAPS
 - DXVAHD_ITELECINE_CAPS
 - dxvahd/DXVAHD_ITELECINE_CAPS
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
 - DXVAHD_ITELECINE_CAPS
---

# DXVAHD_ITELECINE_CAPS enumeration


## -description

Specifies the inverse telecine (IVTC) capabilities of a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.

## -enum-fields

### -field DXVAHD_ITELECINE_CAPS_32:0x1

The video processor can reverse 3:2 pulldown.

### -field DXVAHD_ITELECINE_CAPS_22:0x2

The video processor can reverse 2:2 pulldown.

### -field DXVAHD_ITELECINE_CAPS_2224:0x4

The video processor can reverse 2:2:2:4 pulldown.

### -field DXVAHD_ITELECINE_CAPS_2332:0x8

The video processor can reverse 2:3:3:2 pulldown.

### -field DXVAHD_ITELECINE_CAPS_32322:0x10

The video processor can reverse 3:2:3:2:2 pulldown.

### -field DXVAHD_ITELECINE_CAPS_55:0x20

The video processor can reverse 5:5 pulldown.

### -field DXVAHD_ITELECINE_CAPS_64:0x40

The video processor can reverse 6:4 pulldown.

### -field DXVAHD_ITELECINE_CAPS_87:0x80

The video processor can reverse 8:7 pulldown.

### -field DXVAHD_ITELECINE_CAPS_222222222223:0x100

The video processor can reverse 2:2:2:2:2:2:2:2:2:2:2:3 pulldown.

### -field DXVAHD_ITELECINE_CAPS_OTHER:0x80000000

The video processor can reverse other telecine modes not listed here.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/medfound/direct3d-video-enumerations">Direct3D Video Enumerations</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
