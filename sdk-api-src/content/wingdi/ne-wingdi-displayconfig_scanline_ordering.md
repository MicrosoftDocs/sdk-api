---
UID: NE:wingdi.__unnamed_enum_1
title: DISPLAYCONFIG_SCANLINE_ORDERING (wingdi.h)
description: The DISPLAYCONFIG_SCANLINE_ORDERING enumeration specifies the method that the display uses to create an image on a screen.
helpviewer_keywords: ["CCD_Enumerations_e6c7a4af-750c-4a3c-a89d-562448487abc.xml","DISPLAYCONFIG_SCANLINE_ORDERING","DISPLAYCONFIG_SCANLINE_ORDERING enumeration [Display Devices]","DISPLAYCONFIG_SCANLINE_ORDERING_FORCE_UINT32","DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED","DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED_LOWERFIELDFIRST","DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED_UPPERFIELDFIRST","DISPLAYCONFIG_SCANLINE_ORDERING_PROGRESSIVE","DISPLAYCONFIG_SCANLINE_ORDERING_UNSPECIFIED","display.displayconfig_scanline_ordering","wingdi/DISPLAYCONFIG_SCANLINE_ORDERING","wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_FORCE_UINT32","wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED","wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED_LOWERFIELDFIRST","wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED_UPPERFIELDFIRST","wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_PROGRESSIVE","wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_UNSPECIFIED"]
old-location: display\displayconfig_scanline_ordering.htm
tech.root: display
ms.assetid: 5b8d6c83-e8fb-4529-8d61-557ed0e4da37
ms.date: 12/05/2018
ms.keywords: CCD_Enumerations_e6c7a4af-750c-4a3c-a89d-562448487abc.xml, DISPLAYCONFIG_SCANLINE_ORDERING, DISPLAYCONFIG_SCANLINE_ORDERING enumeration [Display Devices], DISPLAYCONFIG_SCANLINE_ORDERING_FORCE_UINT32, DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED, DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED_LOWERFIELDFIRST, DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED_UPPERFIELDFIRST, DISPLAYCONFIG_SCANLINE_ORDERING_PROGRESSIVE, DISPLAYCONFIG_SCANLINE_ORDERING_UNSPECIFIED, display.displayconfig_scanline_ordering, wingdi/DISPLAYCONFIG_SCANLINE_ORDERING, wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_FORCE_UINT32, wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED, wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED_LOWERFIELDFIRST, wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED_UPPERFIELDFIRST, wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_PROGRESSIVE, wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_UNSPECIFIED
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
req.typenames: DISPLAYCONFIG_SCANLINE_ORDERING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPLAYCONFIG_SCANLINE_ORDERING
 - wingdi/DISPLAYCONFIG_SCANLINE_ORDERING
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
 - DISPLAYCONFIG_SCANLINE_ORDERING
---

# DISPLAYCONFIG_SCANLINE_ORDERING enumeration


## -description

The DISPLAYCONFIG_SCANLINE_ORDERING enumeration specifies the method that the display uses to create an image on a screen.

## -enum-fields

### -field DISPLAYCONFIG_SCANLINE_ORDERING_UNSPECIFIED:0

Indicates that scan-line ordering of the output is unspecified. The caller can only set the <b>scanLineOrdering</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_target_info">DISPLAYCONFIG_PATH_TARGET_INFO</a> structure in a call to the <a href="/windows/desktop/api/winuser/nf-winuser-setdisplayconfig">SetDisplayConfig</a> function to DISPLAYCONFIG_SCANLINE_ORDERING_UNSPECIFIED if the caller also set the refresh rate denominator and numerator of the <b>refreshRate</b> member both to zero. In this case, <b>SetDisplayConfig</b> uses the best refresh rate it can find.

### -field DISPLAYCONFIG_SCANLINE_ORDERING_PROGRESSIVE:1

Indicates that the output is a progressive image.

### -field DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED:2

Indicates that the output is an interlaced image that is created beginning with the upper field.

### -field DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED_UPPERFIELDFIRST

Indicates that the output is an interlaced image that is created beginning with the upper field.

### -field DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED_LOWERFIELDFIRST:3

Indicates that the output is an interlaced image that is created beginning with the lower field.

### -field DISPLAYCONFIG_SCANLINE_ORDERING_FORCE_UINT32:0xFFFFFFFF

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value.
