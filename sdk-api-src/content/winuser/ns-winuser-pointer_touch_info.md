---
UID: NS:winuser.tagPOINTER_TOUCH_INFO
title: POINTER_TOUCH_INFO (winuser.h)
description: Defines basic touch information common to all pointer types.
helpviewer_keywords: ["POINTER_TOUCH_INFO","POINTER_TOUCH_INFO structure [Input Messages and Notifications]","_POINTER_TOUCH_INFO","inputmsg.pointer_touch_info_struct","winuser/POINTER_TOUCH_INFO"]
old-location: inputmsg\pointer_touch_info_struct.htm
tech.root: InputMsg
ms.assetid: fee176ba-ad07-3141-ab4d-1b8c335fd102
ms.date: 12/05/2018
ms.keywords: POINTER_TOUCH_INFO, POINTER_TOUCH_INFO structure [Input Messages and Notifications], _POINTER_TOUCH_INFO, inputmsg.pointer_touch_info_struct, winuser/POINTER_TOUCH_INFO
req.header: winuser.h
req.include-header: Windows.h
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
req.typenames: POINTER_TOUCH_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPOINTER_TOUCH_INFO
 - winuser/tagPOINTER_TOUCH_INFO
 - POINTER_TOUCH_INFO
 - winuser/POINTER_TOUCH_INFO
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
 - POINTER_TOUCH_INFO
---

# POINTER_TOUCH_INFO structure

## -description

Defines basic touch information common to all pointer types.

## -struct-fields

### -field pointerInfo

Type: **[POINTER_INFO](ns-winuser-pointer_info.md)**

An embedded [POINTER_INFO](ns-winuser-pointer_info.md) header structure.

### -field touchFlags

Type: **[Touch Flags](/windows/win32/inputmsg/touch-flags-constants)**

Currently none.

### -field touchMask

Type: **[Touch Mask](/windows/win32/inputmsg/touch-mask-constants)**

Indicates which of the optional fields contain valid values. The member can be zero or any combination of the values from the [Touch Mask](/windows/win32/inputmsg/touch-mask-constants) constants.

### -field rcContact

Type: **RECT**

The predicted screen coordinates of the contact area, in pixels.
By default, if the device does not report a contact area, this field defaults to a 0-by-0 rectangle centered around the pointer location.

The predicted value is based on the pointer position reported by the digitizer and the motion of the pointer. This correction can compensate for visual lag due to inherent delays in sensing and processing the pointer location on the digitizer. This is applicable to  pointers of type [PT_TOUCH](ne-winuser-tagpointer_input_type.md).

### -field rcContactRaw

Type: **RECT**

The raw screen coordinates of the contact area, in pixels. For adjusted screen coordinates, see **rcContact**.

### -field orientation

Type: **UINT32**

A pointer orientation, with a value between 0 and 359, where 0 indicates a touch pointer aligned with the x-axis and pointing from left to right; increasing values indicate degrees of rotation in the clockwise direction.

This field defaults to 0 if the device does not report orientation.

> [!NOTE]
> Some touchscreen devices that support orientation will only report half-range (0-180°) values, while other devices will only report full-range (0-359°) values.

### -field pressure

Type: **UINT32**

 A pen pressure normalized to a range between 0 and 1024. The default is 512.

## -see-also

[Structures](/windows/win32/winrt/structures)
