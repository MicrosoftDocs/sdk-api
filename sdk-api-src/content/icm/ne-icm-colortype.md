---
UID: NE:icm.__unnamed_enum_0
title: COLORTYPE
description: The values of the **COLORTYPE** enumeration are used by several WCS functions. Variables of type **COLOR** are defined in the color spaces enumerated by the **COLORTYPE** enumeration.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: icm.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - icm.h
api_name:
 - COLORTYPE
f1_keywords:
 - COLORTYPE
 - icm/COLORTYPE
dev_langs:
 - c++
---

## -description

The values of the **COLORTYPE** enumeration are used by several WCS functions. Variables of type **COLOR** are defined in the color spaces enumerated by the **COLORTYPE** enumeration.

## -enum-fields

### -field COLOR_GRAY:1

The **COLOR** is in the GRAYCOLOR color space.

### -field COLOR_RGB

The **COLOR** is in the RGBCOLOR color space.

### -field COLOR_XYZ

The **COLOR** is in the XYZCOLOR color space.

### -field COLOR_Yxy

The **COLOR** is in the YxyCOLOR color space.

### -field COLOR_Lab

The **COLOR** is in the LabCOLOR color space.

### -field COLOR_3_CHANNEL

The **COLOR** is in the GENERIC3CHANNEL color space.

### -field COLOR_CMYK

The **COLOR** is in the CMYKCOLOR color space.

### -field COLOR_5_CHANNEL

The **COLOR** is in a five channel color space.

### -field COLOR_6_CHANNEL

The **COLOR** is in a six channel color space.

### -field COLOR_7_CHANNEL

The **COLOR** is in a seven channel color space.

### -field COLOR_8_CHANNEL

The **COLOR** is in an eight channel color space.

### -field COLOR_NAMED

The **COLOR** is in a named color space.

## -remarks

In addition to managing the common two, three, and four channel color spaces, WCS 1.0 is able to perform color management with device profiles that contain five through eight [color channels](/windows/win32/wcs/c). It is also able to use named color spaces. When five, six, seven, or eight color channels are used, the provider of the device profile is free to determine what the color channels represent. The same is true of named color spaces. WCS 1.0 is able to manage these color spaces as long as there is a mapping in the device profile that maps the channels or the name space into the [PCS](/windows/win32/wcs/p). The device profile must also contain a mapping from the PCS into the five, size, seven, or eight channel space, or into the named color space.

## -see-also
