---
UID: NS:winuser.tagPOINTER_TOUCH_INFO
title: POINTER_TOUCH_INFO (winuser.h)
author: windows-sdk-content
description: Defines basic touch information common to all pointer types.
old-location: inputmsg\pointer_touch_info_struct.htm
tech.root: InputMsg
ms.assetid: fee176ba-ad07-3141-ab4d-1b8c335fd102
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: POINTER_TOUCH_INFO, POINTER_TOUCH_INFO structure [Input Messages and Notifications], _POINTER_TOUCH_INFO, inputmsg.pointer_touch_info_struct, winuser/POINTER_TOUCH_INFO
ms.topic: struct
f1_keywords: 
 - "winuser/POINTER_TOUCH_INFO"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - POINTER_TOUCH_INFO
product: Windows
targetos: Windows
req.typenames: POINTER_TOUCH_INFO
req.redist: 
ms.custom: 19H1
---

# POINTER_TOUCH_INFO structure


## -description


Defines basic touch information common to all pointer types.


## -struct-fields




### -field pointerInfo

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-pointer_info">POINTER_INFO</a></b>

An embedded <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-pointer_info">POINTER_INFO</a> header structure.


### -field touchFlags

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/inputmsg/touch-flags-constants">Touch Flags</a></b>

Currently none.


### -field touchMask

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/inputmsg/touch-mask-constants">Touch Mask</a></b>

Indicates which of the optional fields contain valid values. The member can be zero or any combination of the values from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/inputmsg/touch-mask-constants">Touch Mask</a> constants.


### -field rcContact

Type: <b>RECT</b>

 The predicted screen coordinates of the contact area, in pixels.
By default, if the device does not report a contact area, this field defaults to a 0-by-0 rectangle centered around the pointer location.


The predicted value is based on the pointer position reported by the digitizer and the motion of the pointer. This correction can compensate for visual lag due to inherent delays in sensing and processing the pointer location on the digitizer. This is applicable to  pointers of type <a href="https://docs.microsoft.com/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">PT_TOUCH</a>. 


### -field rcContactRaw

Type: <b>RECT</b>

The raw screen coordinates of the contact area, in pixels. For adjusted screen coordinates, see <b>rcContact</b>.


### -field orientation

Type: <b>UINT32</b>

A pointer orientation, with a value between 0 and 359, where 0 indicates a touch pointer aligned with the x-axis and pointing from left to right; increasing values indicate degrees of rotation in the clockwise direction.

This field defaults to 0 if the device does not report orientation.


### -field pressure

Type: <b>UINT32</b>

 A pen pressure normalized to a range between 0 and 1024. The default is 0 if the device does not report pressure.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/inputmsg/structures">Structures</a>
 

 

