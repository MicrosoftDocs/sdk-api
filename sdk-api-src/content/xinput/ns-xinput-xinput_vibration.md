---
UID: NS:xinput._XINPUT_VIBRATION
title: XINPUT_VIBRATION (xinput.h)
description: Specifies motor speed levels for the vibration function of a controller.
helpviewer_keywords: ["*PXINPUT_VIBRATION","PXINPUT_VIBRATION","PXINPUT_VIBRATION structure pointer [XInput Game Controller APIs]","XINPUT_VIBRATION","XINPUT_VIBRATION structure [XInput Game Controller APIs]","xinput.xinput_vibration","xinput/PXINPUT_VIBRATION","xinput/XINPUT_VIBRATION"]
old-location: xinput\xinput_vibration.htm
tech.root: xinput
ms.assetid: T:Microsoft.directx_sdk.reference.XINPUT_VIBRATION
ms.date: 12/05/2018
ms.keywords: '*PXINPUT_VIBRATION, PXINPUT_VIBRATION, PXINPUT_VIBRATION structure pointer [XInput Game Controller APIs], XINPUT_VIBRATION, XINPUT_VIBRATION structure [XInput Game Controller APIs], xinput.xinput_vibration, xinput/PXINPUT_VIBRATION, xinput/XINPUT_VIBRATION'
req.header: xinput.h
req.include-header: 
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
req.typenames: XINPUT_VIBRATION, *PXINPUT_VIBRATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _XINPUT_VIBRATION
 - xinput/_XINPUT_VIBRATION
 - PXINPUT_VIBRATION
 - xinput/PXINPUT_VIBRATION
 - XINPUT_VIBRATION
 - xinput/XINPUT_VIBRATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - XInput.h
api_name:
 - XINPUT_VIBRATION
---

# XINPUT_VIBRATION structure


## -description

Specifies motor speed levels for the vibration function of a controller.

## -struct-fields

### -field wLeftMotorSpeed

Speed of the left motor. Valid values are in the range 0 to 65,535. Zero signifies no motor use; 65,535 signifies 100 percent motor use.

### -field wRightMotorSpeed

Speed of the right motor. Valid values are in the range 0 to 65,535. Zero signifies no motor use; 65,535 signifies 100 percent motor use.

## -remarks

The left motor is the low-frequency rumble motor. The right motor is the high-frequency rumble motor. The two motors are not the same, and they create different vibration effects.

## -see-also

<a href="/windows/desktop/api/xinput/ns-xinput-xinput_gamepad">XINPUT_GAMEPAD</a>



<a href="/windows/desktop/xinput/structures">XInput Structures</a>



<a href="/windows/desktop/api/xinput/nf-xinput-xinputgetcapabilities">XInputGetCapabilities</a>



<a href="/windows/desktop/api/xinput/nf-xinput-xinputsetstate">XInputSetState</a>