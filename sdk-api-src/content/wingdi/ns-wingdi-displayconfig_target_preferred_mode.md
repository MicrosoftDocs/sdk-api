---
UID: NS:wingdi.DISPLAYCONFIG_TARGET_PREFERRED_MODE
title: DISPLAYCONFIG_TARGET_PREFERRED_MODE (wingdi.h)
description: The DISPLAYCONFIG_TARGET_PREFERRED_MODE structure contains information about the preferred mode of a display.
helpviewer_keywords: ["CCD_Structures_d19517fa-c72d-47bf-9198-c447efe1ba90.xml","DISPLAYCONFIG_TARGET_PREFERRED_MODE","DISPLAYCONFIG_TARGET_PREFERRED_MODE structure [Display Devices]","display.displayconfig_target_preferred_mode","wingdi/DISPLAYCONFIG_TARGET_PREFERRED_MODE"]
old-location: display\displayconfig_target_preferred_mode.htm
tech.root: display
ms.assetid: 1a4926ca-36d2-466c-b3d2-b59d34a89ee6
ms.date: 12/05/2018
ms.keywords: CCD_Structures_d19517fa-c72d-47bf-9198-c447efe1ba90.xml, DISPLAYCONFIG_TARGET_PREFERRED_MODE, DISPLAYCONFIG_TARGET_PREFERRED_MODE structure [Display Devices], display.displayconfig_target_preferred_mode, wingdi/DISPLAYCONFIG_TARGET_PREFERRED_MODE
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
req.typenames: DISPLAYCONFIG_TARGET_PREFERRED_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPLAYCONFIG_TARGET_PREFERRED_MODE
 - wingdi/DISPLAYCONFIG_TARGET_PREFERRED_MODE
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
 - DISPLAYCONFIG_TARGET_PREFERRED_MODE
---

# DISPLAYCONFIG_TARGET_PREFERRED_MODE structure


## -description

The <b>DISPLAYCONFIG_TARGET_PREFERRED_MODE</b> structure contains information about the preferred mode of a display.

## -struct-fields

### -field header

A <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_device_info_header">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> structure that contains information about the request for the target preferred mode. The caller should set the <b>type</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER to DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_PREFERRED_MODE and the <b>adapterId</b> and <b>id</b> members of DISPLAYCONFIG_DEVICE_INFO_HEADER to the target for which the caller wants the preferred mode. The caller should set the <b>size</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER to at least the size of the DISPLAYCONFIG_TARGET_PREFERRED_MODE structure.

### -field width

The width in pixels of the best mode for the monitor that is connected to the target that the <b>targetMode</b> member specifies.

### -field height

The height in pixels of the best mode for the monitor that is connected to the target that the <b>targetMode</b> member specifies.

### -field targetMode

A <a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_mode">DISPLAYCONFIG_TARGET_MODE</a> structure that describes the best target mode for the monitor that is connected to the specified target.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_device_info_header">DISPLAYCONFIG_DEVICE_INFO_HEADER</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-displayconfig_target_mode">DISPLAYCONFIG_TARGET_MODE</a>