---
UID: NS:dinputd.DIOBJECTCALIBRATION
title: DIOBJECTCALIBRATION (dinputd.h)
description: The DIOBJECTCALIBRATION structure describes the information contained in the &quot;Calibration&quot; value of the registry key for each axis on a device.
helpviewer_keywords: ["*LPDIOBJECTCALIBRATION","DIOBJECTCALIBRATION","DIOBJECTCALIBRATION structure [Human Input Devices]","di_ref_232167f0-8ec2-4ec7-91aa-169ab5ae5921.xml","dinputd/DIOBJECTCALIBRATION","hid.diobjectcalibration"]
old-location: hid\diobjectcalibration.htm
tech.root: hid
ms.assetid: d1e6a9ee-c7eb-42d1-9f91-185dcccc3109
ms.date: 12/05/2018
ms.keywords: '*LPDIOBJECTCALIBRATION, DIOBJECTCALIBRATION, DIOBJECTCALIBRATION structure [Human Input Devices], di_ref_232167f0-8ec2-4ec7-91aa-169ab5ae5921.xml, dinputd/DIOBJECTCALIBRATION, hid.diobjectcalibration'
req.header: dinputd.h
req.include-header: Dinputd.h
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
req.typenames: DIOBJECTCALIBRATION, *LPDIOBJECTCALIBRATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIOBJECTCALIBRATION
 - dinputd/DIOBJECTCALIBRATION
 - LPDIOBJECTCALIBRATION
 - dinputd/LPDIOBJECTCALIBRATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dinputd.h
api_name:
 - DIOBJECTCALIBRATION
---

# DIOBJECTCALIBRATION structure


## -description

The DIOBJECTCALIBRATION structure describes the information contained in the "Calibration" value of the registry key for each axis on a device.

## -struct-fields

### -field lMin

Specifies the logical value for the axis minimum position.

### -field lCenter

Specifies the logical value for the axis center position.

### -field lMax

Specifies the logical value for the axis maximum position.

## -remarks

If the "Calibration" value is absent, then the calibration information is taken from the joystick [JOYREGHWVALUES](../mmddk/ns-mmddk-joyreghwvalues.md) configuration structure.

Only HID joysticks have a "Calibration" value.