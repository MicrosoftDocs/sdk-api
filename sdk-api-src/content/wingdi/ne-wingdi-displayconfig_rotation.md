---
UID: NE:wingdi.__unnamed_enum_3
title: DISPLAYCONFIG_ROTATION (wingdi.h)
description: The DISPLAYCONFIG_ROTATION enumeration specifies the clockwise rotation of the display.
helpviewer_keywords: ["CCD_Enumerations_6667e997-4697-419d-914d-0fe25a16228b.xml","DISPLAYCONFIG_ROTATION","DISPLAYCONFIG_ROTATION enumeration [Display Devices]","DISPLAYCONFIG_ROTATION_FORCE_UINT32","DISPLAYCONFIG_ROTATION_IDENTITY","DISPLAYCONFIG_ROTATION_ROTATE180","DISPLAYCONFIG_ROTATION_ROTATE270","DISPLAYCONFIG_ROTATION_ROTATE90","display.displayconfig_rotation","wingdi/DISPLAYCONFIG_ROTATION","wingdi/DISPLAYCONFIG_ROTATION_FORCE_UINT32","wingdi/DISPLAYCONFIG_ROTATION_IDENTITY","wingdi/DISPLAYCONFIG_ROTATION_ROTATE180","wingdi/DISPLAYCONFIG_ROTATION_ROTATE270","wingdi/DISPLAYCONFIG_ROTATION_ROTATE90"]
old-location: display\displayconfig_rotation.htm
tech.root: display
ms.assetid: 82709d44-45e6-47ec-9caa-5a947a568c52
ms.date: 12/05/2018
ms.keywords: CCD_Enumerations_6667e997-4697-419d-914d-0fe25a16228b.xml, DISPLAYCONFIG_ROTATION, DISPLAYCONFIG_ROTATION enumeration [Display Devices], DISPLAYCONFIG_ROTATION_FORCE_UINT32, DISPLAYCONFIG_ROTATION_IDENTITY, DISPLAYCONFIG_ROTATION_ROTATE180, DISPLAYCONFIG_ROTATION_ROTATE270, DISPLAYCONFIG_ROTATION_ROTATE90, display.displayconfig_rotation, wingdi/DISPLAYCONFIG_ROTATION, wingdi/DISPLAYCONFIG_ROTATION_FORCE_UINT32, wingdi/DISPLAYCONFIG_ROTATION_IDENTITY, wingdi/DISPLAYCONFIG_ROTATION_ROTATE180, wingdi/DISPLAYCONFIG_ROTATION_ROTATE270, wingdi/DISPLAYCONFIG_ROTATION_ROTATE90
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
req.typenames: DISPLAYCONFIG_ROTATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPLAYCONFIG_ROTATION
 - wingdi/DISPLAYCONFIG_ROTATION
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
 - DISPLAYCONFIG_ROTATION
---

# DISPLAYCONFIG_ROTATION enumeration


## -description

The DISPLAYCONFIG_ROTATION enumeration specifies the clockwise rotation of the display.

## -enum-fields

### -field DISPLAYCONFIG_ROTATION_IDENTITY:1

Indicates that rotation is 0 degrees—landscape mode.

### -field DISPLAYCONFIG_ROTATION_ROTATE90:2

Indicates that rotation is 90 degrees clockwise—portrait mode.

### -field DISPLAYCONFIG_ROTATION_ROTATE180:3

Indicates that rotation is 180 degrees clockwise—inverted landscape mode.

### -field DISPLAYCONFIG_ROTATION_ROTATE270:4

Indicates that rotation is 270 degrees clockwise—inverted portrait mode.

### -field DISPLAYCONFIG_ROTATION_FORCE_UINT32:0xFFFFFFFF

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value.

