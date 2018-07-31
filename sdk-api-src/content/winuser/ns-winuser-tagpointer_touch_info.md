---
UID: NS:winuser.tagPOINTER_TOUCH_INFO
title: tagPOINTER_TOUCH_INFO
author: windows-sdk-content
description: Defines basic touch information common to all pointer types.
old-location: inputmsg\pointer_touch_info_struct.htm
old-project: InputMsg
ms.assetid: fee176ba-ad07-3141-ab4d-1b8c335fd102
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: POINTER_TOUCH_INFO, POINTER_TOUCH_INFO structure [Input Messages and Notifications], _POINTER_TOUCH_INFO, inputmsg.pointer_touch_info_struct, tagPOINTER_TOUCH_INFO, winuser/POINTER_TOUCH_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: POINTER_TOUCH_INFO
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagPOINTER_TOUCH_INFO structure


## -description


Defines basic touch information common to all pointer types.


## -struct-fields




### -field pointerInfo

Type: <b><a href="https://msdn.microsoft.com/fee176ba-ad07-4145-0b4d-1b8c335fd102">POINTER_INFO</a></b>

An embedded <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-0b4d-1b8c335fd102">POINTER_INFO</a> header structure.


### -field touchFlags

Type: <b><a href="https://msdn.microsoft.com/87CE2BF4-BD33-4D45-B001-065048702064">Touch Flags</a></b>

Currently none.


### -field touchMask

Type: <b><a href="https://msdn.microsoft.com/23AD50C8-C769-48D6-9F27-DB2755C03D5C">Touch Mask</a></b>

Indicates which of the optional fields contain valid values. The member can be zero or any combination of the values from the <a href="https://msdn.microsoft.com/23AD50C8-C769-48D6-9F27-DB2755C03D5C">Touch Mask</a> constants.


### -field rcContact

Type: <b>RECT</b>

 The predicted screen coordinates of the contact area, in pixels.
By default, if the device does not report a contact area, this field defaults to a 0-by-0 rectangle centered around the pointer location.


The predicted value is based on the pointer position reported by the digitizer and the motion of the pointer. This correction can compensate for visual lag due to inherent delays in sensing and processing the pointer location on the digitizer. This is applicable to  pointers of type <a href="https://msdn.microsoft.com/3334DCD0-DAE1-4AC2-AB36-23D114803100">PT_TOUCH</a>. 


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




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

