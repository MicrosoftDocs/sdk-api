---
UID: NS:winuser.tagPOINTER_PEN_INFO
title: POINTER_PEN_INFO (winuser.h)
description: Defines basic pen information common to all pointer types.
helpviewer_keywords: ["POINTER_PEN_INFO","POINTER_PEN_INFO structure [Input Messages and Notifications]","_POINTER_PEN_INFO","inputmsg.pointer_pen_info_struct","winuser/POINTER_PEN_INFO"]
old-location: inputmsg\pointer_pen_info_struct.htm
tech.root: InputMsg
ms.assetid: fee176ba-ad07-4141-ab4d-1b8c335fd111
ms.date: 12/05/2018
ms.keywords: POINTER_PEN_INFO, POINTER_PEN_INFO structure [Input Messages and Notifications], _POINTER_PEN_INFO, inputmsg.pointer_pen_info_struct, winuser/POINTER_PEN_INFO
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
req.typenames: POINTER_PEN_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPOINTER_PEN_INFO
 - winuser/tagPOINTER_PEN_INFO
 - POINTER_PEN_INFO
 - winuser/POINTER_PEN_INFO
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
 - POINTER_PEN_INFO
---

# POINTER_PEN_INFO structure


## -description

Defines basic pen information common to all pointer types.

## -struct-fields

### -field pointerInfo

Type: <b>POINTER_INFO</b>

An embedded <a href="/windows/win32/api/winuser/ns-winuser-pointer_info">POINTER_INFO</a> structure.

### -field penFlags

Type: <b>PEN_FLAGS</b>

The pen flag. This member can be zero or any reasonable combination of the values from the <a href="/windows/win32/inputmsg/pen-flags-constants">Pen Flags</a> constants.

### -field penMask

Type: <b>PEN_MASK</b>

The pen mask. This member can be zero or any reasonable combination of the values from the <a href="/windows/win32/inputmsg/pen-mask-constants">Pen Mask</a> constants.

### -field pressure

Type: <b>UINT32</b>

 A pen pressure normalized to a range between 0 and 1024. The default is 0 if the device does not report pressure.

### -field rotation

Type: <b>UINT32</b>

The clockwise rotation, or twist, of the pointer normalized in a range of 0 to 359.
The default is 0.

### -field tiltX

Type: <b>INT32</b>

The angle of tilt of the pointer along the x-axis in a range of -90 to +90, with a positive value indicating a tilt to the right.
The default is 0.

### -field tiltY

Type: <b>INT32</b>

The angle of tilt of the pointer along the y-axis in a range of -90 to +90, with a positive value indicating a tilt toward the user. The default is 0.

## -remarks

Applications can retrieve this information using the <a href="/windows/desktop/api/winuser/nf-winuser-getpointerpeninfo">GetPointerPenInfo</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getpointerframepeninfo">GetPointerFramePenInfo</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getpointerpeninfohistory">GetPointerPenInfoHistory</a> and <a href="/windows/desktop/api/winuser/nf-winuser-getpointerframepeninfohistory">GetPointerFramePenInfoHistory</a> API functions.

## -see-also

<a href="/windows/win32/inputmsg/structures">Structures</a>