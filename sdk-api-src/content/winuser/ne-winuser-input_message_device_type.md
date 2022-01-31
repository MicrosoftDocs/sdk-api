---
UID: NE:winuser.tagINPUT_MESSAGE_DEVICE_TYPE
title: INPUT_MESSAGE_DEVICE_TYPE (winuser.h)
description: The type of device that sent the input message.
helpviewer_keywords: ["IMDT_KEYBOARD","IMDT_MOUSE","IMDT_PEN","IMDT_TOUCH","IMDT_TOUCHPAD","IMDT_UNAVAILABLE","INPUT_MESSAGE_DEVICE_TYPE","INPUT_MESSAGE_DEVICE_TYPE enumeration","input_sourceid.input_message_device_type","inputsourceid.input_message_device_type","winuser/IMDT_KEYBOARD","winuser/IMDT_MOUSE","winuser/IMDT_PEN","winuser/IMDT_TOUCH","winuser/IMDT_TOUCHPAD","winuser/IMDT_UNAVAILABLE","winuser/INPUT_MESSAGE_DEVICE_TYPE"]
old-location: input_sourceid\input_message_device_type.htm
tech.root: controls
ms.assetid: aaaa8d9b-1056-4fa3-afcf-43d2c4b41c0e
ms.date: 12/05/2018
ms.keywords: IMDT_KEYBOARD, IMDT_MOUSE, IMDT_PEN, IMDT_TOUCH, IMDT_TOUCHPAD, IMDT_UNAVAILABLE, INPUT_MESSAGE_DEVICE_TYPE, INPUT_MESSAGE_DEVICE_TYPE enumeration, input_sourceid.input_message_device_type, inputsourceid.input_message_device_type, winuser/IMDT_KEYBOARD, winuser/IMDT_MOUSE, winuser/IMDT_PEN, winuser/IMDT_TOUCH, winuser/IMDT_TOUCHPAD, winuser/IMDT_UNAVAILABLE, winuser/INPUT_MESSAGE_DEVICE_TYPE
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
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
req.typenames: INPUT_MESSAGE_DEVICE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagINPUT_MESSAGE_DEVICE_TYPE
 - winuser/tagINPUT_MESSAGE_DEVICE_TYPE
 - INPUT_MESSAGE_DEVICE_TYPE
 - winuser/INPUT_MESSAGE_DEVICE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winuser.h
api_name:
 - INPUT_MESSAGE_DEVICE_TYPE
---

# INPUT_MESSAGE_DEVICE_TYPE enumeration


## -description

The type of device that sent the input message.

## -enum-fields

### -field IMDT_UNAVAILABLE:0x00000000

The device type isn't identified.

### -field IMDT_KEYBOARD:0x00000001

Keyboard input.

### -field IMDT_MOUSE:0x00000002

Mouse input.

### -field IMDT_TOUCH:0x00000004

Touch input.

### -field IMDT_PEN:0x00000008

Pen or stylus input.

### -field IMDT_TOUCHPAD:0x00000010

Touchpad input (Windows 8.1 and later).

## -see-also

<a href="/previous-versions/windows/desktop/input_sourceid/enumerations">Enumerations</a>
