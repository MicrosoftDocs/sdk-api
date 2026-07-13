---
UID: NS:xinput._XINPUT_STATE
title: XINPUT_STATE (xinput.h)
description: Represents the state of a controller.
helpviewer_keywords: ["*PXINPUT_STATE","PXINPUT_STATE","PXINPUT_STATE structure pointer [XInput Game Controller APIs]","XINPUT_STATE","XINPUT_STATE structure [XInput Game Controller APIs]","xinput.xinput_state","xinput/PXINPUT_STATE","xinput/XINPUT_STATE"]
old-location: xinput\xinput_state.htm
tech.root: xinput
ms.assetid: T:Microsoft.directx_sdk.reference.XINPUT_STATE
ms.date: 12/05/2018
ms.keywords: '*PXINPUT_STATE, PXINPUT_STATE, PXINPUT_STATE structure pointer [XInput Game Controller APIs], XINPUT_STATE, XINPUT_STATE structure [XInput Game Controller APIs], xinput.xinput_state, xinput/PXINPUT_STATE, xinput/XINPUT_STATE'
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
req.typenames: XINPUT_STATE, *PXINPUT_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _XINPUT_STATE
 - xinput/_XINPUT_STATE
 - PXINPUT_STATE
 - xinput/PXINPUT_STATE
 - XINPUT_STATE
 - xinput/XINPUT_STATE
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
 - XINPUT_STATE
---

# XINPUT_STATE structure


## -description

Represents the state of a controller.

## -struct-fields

### -field dwPacketNumber

State packet number. The packet number indicates whether there have been any changes in the state of the controller. If the <i>dwPacketNumber</i> member is the same in sequentially returned <b>XINPUT_STATE</b> structures, the controller state has not changed.

### -field Gamepad

<a href="/windows/desktop/api/xinput/ns-xinput-xinput_gamepad">XINPUT_GAMEPAD</a> structure containing the current state of a controller.

## -remarks

The <i>dwPacketNumber</i> member is incremented only if the status of the controller has changed since the controller was last polled.

## -see-also

<a href="/windows/desktop/api/xinput/ns-xinput-xinput_gamepad">XINPUT_GAMEPAD</a>



<a href="/windows/desktop/xinput/structures">XInput Structures</a>



<a href="/windows/desktop/api/xinput/nf-xinput-xinputgetstate">XInputGetState</a>