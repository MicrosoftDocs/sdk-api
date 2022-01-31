---
UID: NE:winuser.tagPOINTER_DEVICE_CURSOR_TYPE
title: POINTER_DEVICE_CURSOR_TYPE (winuser.h)
description: Identifies the pointer device cursor types.
helpviewer_keywords: ["POINTER_DEVICE_CURSOR_TYPE","POINTER_DEVICE_CURSOR_TYPE enumeration","POINTER_DEVICE_CURSOR_TYPE_ERASER","POINTER_DEVICE_CURSOR_TYPE_MAX","POINTER_DEVICE_CURSOR_TYPE_TIP","POINTER_DEVICE_CURSOR_TYPE_UNKNOWN","input_pointerdevice.pointer_device_cursor_type","unifiedinputstack.pointer_device_cursor_type","winuser/POINTER_DEVICE_CURSOR_TYPE","winuser/POINTER_DEVICE_CURSOR_TYPE_ERASER","winuser/POINTER_DEVICE_CURSOR_TYPE_MAX","winuser/POINTER_DEVICE_CURSOR_TYPE_TIP","winuser/POINTER_DEVICE_CURSOR_TYPE_UNKNOWN"]
old-location: input_pointerdevice\pointer_device_cursor_type.htm
tech.root: controls
ms.assetid: ebd5c0c6-a949-42f1-976e-96d143b1a0d7
ms.date: 12/05/2018
ms.keywords: POINTER_DEVICE_CURSOR_TYPE, POINTER_DEVICE_CURSOR_TYPE enumeration, POINTER_DEVICE_CURSOR_TYPE_ERASER, POINTER_DEVICE_CURSOR_TYPE_MAX, POINTER_DEVICE_CURSOR_TYPE_TIP, POINTER_DEVICE_CURSOR_TYPE_UNKNOWN, input_pointerdevice.pointer_device_cursor_type, unifiedinputstack.pointer_device_cursor_type, winuser/POINTER_DEVICE_CURSOR_TYPE, winuser/POINTER_DEVICE_CURSOR_TYPE_ERASER, winuser/POINTER_DEVICE_CURSOR_TYPE_MAX, winuser/POINTER_DEVICE_CURSOR_TYPE_TIP, winuser/POINTER_DEVICE_CURSOR_TYPE_UNKNOWN
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: POINTER_DEVICE_CURSOR_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPOINTER_DEVICE_CURSOR_TYPE
 - winuser/tagPOINTER_DEVICE_CURSOR_TYPE
 - POINTER_DEVICE_CURSOR_TYPE
 - winuser/POINTER_DEVICE_CURSOR_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - POINTER_DEVICE_CURSOR_TYPE
---

# POINTER_DEVICE_CURSOR_TYPE enumeration


## -description

Identifies the pointer device cursor types.

## -enum-fields

### -field POINTER_DEVICE_CURSOR_TYPE_UNKNOWN:0x00000000

Unidentified cursor.

### -field POINTER_DEVICE_CURSOR_TYPE_TIP:0x00000001

Pen tip.

### -field POINTER_DEVICE_CURSOR_TYPE_ERASER:0x00000002

Pen eraser.

### -field POINTER_DEVICE_CURSOR_TYPE_MAX:0xFFFFFFFF

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value.

## -remarks

Cursor objects represent pointing and selecting devices used with digitizer devices, most commonly tactile contacts on touch digitizers and tablet pens on pen digitizers. Physical pens may have multiple tips (such as normal and eraser ends), with each pen tip representing a different cursor object. Each cursor object has an associated cursor identifier.

## -see-also

<a href="/previous-versions/windows/desktop/input_pointerdevice/enumerations">Enumerations</a>
