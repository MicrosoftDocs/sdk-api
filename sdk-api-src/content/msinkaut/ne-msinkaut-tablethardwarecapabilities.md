---
UID: NE:msinkaut.TabletHardwareCapabilities
title: TabletHardwareCapabilities (msinkaut.h)
description: Specifies the hardware capabilities of the Tablet PC.
helpviewer_keywords: ["THWC_CursorMustTouch","THWC_CursorsHavePhysicalIds","THWC_HardProximity","THWC_Integrated","TabletHardwareCapabilities","TabletHardwareCapabilities enumeration [Tablet PC]","ab8dfca3-df5e-40a7-9da2-d19447bc746b","msinkaut/THWC_CursorMustTouch","msinkaut/THWC_CursorsHavePhysicalIds","msinkaut/THWC_HardProximity","msinkaut/THWC_Integrated","msinkaut/TabletHardwareCapabilities","tablet.tablethardwarecapabilities"]
old-location: tablet\tablethardwarecapabilities.htm
tech.root: tablet
ms.assetid: ab8dfca3-df5e-40a7-9da2-d19447bc746b
ms.date: 12/05/2018
ms.keywords: THWC_CursorMustTouch, THWC_CursorsHavePhysicalIds, THWC_HardProximity, THWC_Integrated, TabletHardwareCapabilities, TabletHardwareCapabilities enumeration [Tablet PC], ab8dfca3-df5e-40a7-9da2-d19447bc746b, msinkaut/THWC_CursorMustTouch, msinkaut/THWC_CursorsHavePhysicalIds, msinkaut/THWC_HardProximity, msinkaut/THWC_Integrated, msinkaut/TabletHardwareCapabilities, tablet.tablethardwarecapabilities
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: TabletHardwareCapabilities
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TabletHardwareCapabilities
 - msinkaut/TabletHardwareCapabilities
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - TabletHardwareCapabilities
---

# TabletHardwareCapabilities enumeration


## -description

Specifies the hardware capabilities of the Tablet PC.

## -enum-fields

### -field THWC_Integrated:0x1

The digitizer is integrated with the display.

### -field THWC_CursorMustTouch:0x2

The cursor must be in physical contact with the device to report position.

### -field THWC_HardProximity:0x4

The device can generate in-air packets when the cursor is in the physical detection range (proximity) of the device.

### -field THWC_CursorsHavePhysicalIds:0x8

The device can uniquely identify the active cursor.

## -remarks

In C++, explicit casting is required when trying to set more than one flag at a time. A compilation error occurs if explicit casting is not used.

The value is 0 if the tablet device cannot provide this information.

This enumeration is a flag.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-get_hardwarecapabilities">HardwareCapabilities Property</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a>
