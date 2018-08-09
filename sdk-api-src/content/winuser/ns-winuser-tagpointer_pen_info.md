---
UID: NS:winuser.tagPOINTER_PEN_INFO
title: tagPOINTER_PEN_INFO
author: windows-sdk-content
description: Defines basic pen information common to all pointer types.
old-location: inputmsg\pointer_pen_info_struct.htm
old-project: InputMsg
ms.assetid: fee176ba-ad07-4141-ab4d-1b8c335fd111
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: POINTER_PEN_INFO, POINTER_PEN_INFO structure [Input Messages and Notifications], _POINTER_PEN_INFO, inputmsg.pointer_pen_info_struct, tagPOINTER_PEN_INFO, winuser/POINTER_PEN_INFO
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
req.typenames: POINTER_PEN_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - POINTER_PEN_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagPOINTER_PEN_INFO structure


## -description


Defines basic pen information common to all pointer types. 


## -struct-fields




### -field pointerInfo

Type: <b>POINTER_INFO</b>

An embedded <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-0b4d-1b8c335fd102">POINTER_INFO</a> structure.


### -field penFlags

Type: <b>PEN_FLAGS</b>

The pen flag. This member can be zero or any reasonable combination of the values from the <a href="https://msdn.microsoft.com/BC3CE568-4090-4451-B780-18530C988305">Pen Flags</a> constants.


### -field penMask

Type: <b>PEN_MASK</b>

The pen mask. This member can be zero or any reasonable combination of the values from the <a href="https://msdn.microsoft.com/6A44B701-55E1-41D4-9C4A-807E57441DA4">Pen Mask</a> constants.


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



Applications can retrieve this information using the <a href="https://msdn.microsoft.com/5f1f7252-a4aa-4b06-94c9-2aa365cf0100">GetPointerPenInfo</a>, <a href="https://msdn.microsoft.com/52db9b96-7f9e-41d7-88f7-b9c7691a6511">GetPointerFramePenInfo</a>, <a href="https://msdn.microsoft.com/90082327-b242-4f5d-8cd7-fd8ef9340395">GetPointerPenInfoHistory</a> and <a href="https://msdn.microsoft.com/a4f6a9f3-dfbd-4413-aae7-f58e1521ef1d">GetPointerFramePenInfoHistory</a> API functions.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

