---
UID: NE:wingdi.__unnamed_enum_5
title: DISPLAYCONFIG_PIXELFORMAT (wingdi.h)
description: The DISPLAYCONFIG_PIXELFORMAT enumeration specifies pixel format in various bits per pixel (BPP) values.
helpviewer_keywords: ["CCD_Enumerations_d2979717-6f47-4872-9be2-8b19b06ce2f2.xml","DISPLAYCONFIG_PIXELFORMAT","DISPLAYCONFIG_PIXELFORMAT enumeration [Display Devices]","DISPLAYCONFIG_PIXELFORMAT_16BPP","DISPLAYCONFIG_PIXELFORMAT_24BPP","DISPLAYCONFIG_PIXELFORMAT_32BPP","DISPLAYCONFIG_PIXELFORMAT_8BPP","DISPLAYCONFIG_PIXELFORMAT_FORCE_UINT32","DISPLAYCONFIG_PIXELFORMAT_NONGDI","display.displayconfig_pixelformat","wingdi/DISPLAYCONFIG_PIXELFORMAT","wingdi/DISPLAYCONFIG_PIXELFORMAT_16BPP","wingdi/DISPLAYCONFIG_PIXELFORMAT_24BPP","wingdi/DISPLAYCONFIG_PIXELFORMAT_32BPP","wingdi/DISPLAYCONFIG_PIXELFORMAT_8BPP","wingdi/DISPLAYCONFIG_PIXELFORMAT_FORCE_UINT32","wingdi/DISPLAYCONFIG_PIXELFORMAT_NONGDI"]
old-location: display\displayconfig_pixelformat.htm
tech.root: display
ms.assetid: dca8433d-89a9-492c-bebb-6a28f485896c
ms.date: 12/05/2018
ms.keywords: CCD_Enumerations_d2979717-6f47-4872-9be2-8b19b06ce2f2.xml, DISPLAYCONFIG_PIXELFORMAT, DISPLAYCONFIG_PIXELFORMAT enumeration [Display Devices], DISPLAYCONFIG_PIXELFORMAT_16BPP, DISPLAYCONFIG_PIXELFORMAT_24BPP, DISPLAYCONFIG_PIXELFORMAT_32BPP, DISPLAYCONFIG_PIXELFORMAT_8BPP, DISPLAYCONFIG_PIXELFORMAT_FORCE_UINT32, DISPLAYCONFIG_PIXELFORMAT_NONGDI, display.displayconfig_pixelformat, wingdi/DISPLAYCONFIG_PIXELFORMAT, wingdi/DISPLAYCONFIG_PIXELFORMAT_16BPP, wingdi/DISPLAYCONFIG_PIXELFORMAT_24BPP, wingdi/DISPLAYCONFIG_PIXELFORMAT_32BPP, wingdi/DISPLAYCONFIG_PIXELFORMAT_8BPP, wingdi/DISPLAYCONFIG_PIXELFORMAT_FORCE_UINT32, wingdi/DISPLAYCONFIG_PIXELFORMAT_NONGDI
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 Client.
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
req.typenames: DISPLAYCONFIG_PIXELFORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPLAYCONFIG_PIXELFORMAT
 - wingdi/DISPLAYCONFIG_PIXELFORMAT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wingdi.h
api_name:
 - DISPLAYCONFIG_PIXELFORMAT
---

# DISPLAYCONFIG_PIXELFORMAT enumeration


## -description

The DISPLAYCONFIG_PIXELFORMAT enumeration specifies pixel format in various bits per pixel (BPP) values.

## -enum-fields

### -field DISPLAYCONFIG_PIXELFORMAT_8BPP:1

Indicates 8 BPP format.

### -field DISPLAYCONFIG_PIXELFORMAT_16BPP:2

Indicates 16 BPP format.

### -field DISPLAYCONFIG_PIXELFORMAT_24BPP:3

Indicates 24 BPP format.

### -field DISPLAYCONFIG_PIXELFORMAT_32BPP:4

Indicates 32 BPP format.

### -field DISPLAYCONFIG_PIXELFORMAT_NONGDI:5

Indicates that the current display is not an 8, 16, 24, or 32 BPP GDI desktop mode. For example, a call to the <a href="/windows/desktop/api/winuser/nf-winuser-querydisplayconfig">QueryDisplayConfig</a> function returns DISPLAYCONFIG_PIXELFORMAT_NONGDI if a DirectX application previously set the desktop to A2R10G10B10 format. A call to the <a href="/windows/desktop/api/winuser/nf-winuser-setdisplayconfig">SetDisplayConfig</a> function fails if any pixel formats for active paths are set to DISPLAYCONFIG_PIXELFORMAT_NONGDI.

### -field DISPLAYCONFIG_PIXELFORMAT_FORCE_UINT32:0xffffffff

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-querydisplayconfig">QueryDisplayConfig</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setdisplayconfig">SetDisplayConfig</a>
