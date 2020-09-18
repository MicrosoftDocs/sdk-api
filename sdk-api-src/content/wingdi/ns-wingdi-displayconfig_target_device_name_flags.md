---
UID: NS:wingdi.DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS
title: DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS (wingdi.h)
description: The DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS structure contains information about a target device.
helpviewer_keywords: ["CCD_Structures_a8452615-b845-4ecd-92d4-6e18e8bef145.xml","DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS","DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS structure [Display Devices]","display.displayconfig_target_device_name_flags","wingdi/DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS"]
old-location: display\displayconfig_target_device_name_flags.htm
tech.root: display
ms.assetid: f0318dd3-4350-4de3-84c8-2c998254c68c
ms.date: 12/05/2018
ms.keywords: CCD_Structures_a8452615-b845-4ecd-92d4-6e18e8bef145.xml, DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS, DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS structure [Display Devices], display.displayconfig_target_device_name_flags, wingdi/DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS
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
req.typenames: DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS
 - wingdi/DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS
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
 - DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS
---

# DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS structure


## -description

The <b>DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS</b> structure contains information about a target device.

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.friendlyNameFromEdid

A UINT32 value that indicates that the string in the <b>monitorFriendlyDeviceName</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_device_name">DISPLAYCONFIG_TARGET_DEVICE_NAME</a> structure was constructed from the manufacture identification string in the extended display identification data (EDID).

Setting this member is equivalent to setting the first bit of the 32-bit <b>value</b> member (0x00000001).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.friendlyNameForced

A UINT32 value that indicates that the target is forced with no detectable monitor attached and the <b>monitorFriendlyDeviceName</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_device_name">DISPLAYCONFIG_TARGET_DEVICE_NAME</a> structure is a NULL-terminated empty string.

Setting this member is equivalent to setting the second bit of the 32-bit <b>value</b> member (0x00000002).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.edidIdsValid

A UINT32 value that indicates that the <b>edidManufactureId</b> and <b>edidProductCodeId</b> members of the <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_device_name">DISPLAYCONFIG_TARGET_DEVICE_NAME</a> structure are valid and were obtained from the EDID.

Setting this member is equivalent to setting the third bit of the 32-bit <b>value</b> member (0x00000004).

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.reserved

This member is reserved and should be set to zero. Setting this member to zero is equivalent to setting the remaining 29 bits (0xFFFFFFF8) of the 32-bit <b>value</b> member to zeros.

### -field DUMMYUNIONNAME.value

A member in the union that DISPLAYCONFIG_TARGET_DEVICE_NAME_FLAGS contains that can hold a 32-bit value that identifies information about the device.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_device_name">DISPLAYCONFIG_TARGET_DEVICE_NAME</a>