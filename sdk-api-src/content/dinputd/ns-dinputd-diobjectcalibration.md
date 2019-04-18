---
UID: NS:dinputd.DIOBJECTCALIBRATION
title: DIOBJECTCALIBRATION (dinputd.h)
author: windows-sdk-content
description: The DIOBJECTCALIBRATION structure describes the information contained in the &#0034;Calibration&#0034; value of the registry key for each axis on a device.
old-location: hid\diobjectcalibration.htm
tech.root: hid
ms.assetid: d1e6a9ee-c7eb-42d1-9f91-185dcccc3109
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDIOBJECTCALIBRATION, DIOBJECTCALIBRATION, DIOBJECTCALIBRATION structure [Human Input Devices], di_ref_232167f0-8ec2-4ec7-91aa-169ab5ae5921.xml, dinputd/DIOBJECTCALIBRATION, hid.diobjectcalibration"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dinputd.h
api_name:
 - DIOBJECTCALIBRATION
product: Windows
targetos: Windows
req.typenames: DIOBJECTCALIBRATION, *LPDIOBJECTCALIBRATION
req.redist: 
ms.custom: 19H1
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



If the "Calibration" value is absent, then the calibration information is taken from the joystick <a href="https://msdn.microsoft.com/cd59611f-7bf2-4bba-80dc-f54c815af3e6">JOYREGHWVALUES</a> configuration structure.

Only HID joysticks have a "Calibration" value.



