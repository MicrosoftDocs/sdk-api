---
UID: NE:winuser.tagPOINTER_DEVICE_TYPE
title: POINTER_DEVICE_TYPE (winuser.h)
author: windows-sdk-content
description: Identifies the pointer device types.
old-location: input_pointerdevice\pointer_device_type.htm
tech.root: Input_PointerDevice
ms.assetid: 7702adec-e24f-4dc8-b5d4-f1f9dbcb5ed0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: POINTER_DEVICE_TYPE, POINTER_DEVICE_TYPE enumeration, POINTER_DEVICE_TYPE_EXTERNAL_PEN, POINTER_DEVICE_TYPE_INTEGRATED_PEN, POINTER_DEVICE_TYPE_MAX, POINTER_DEVICE_TYPE_TOUCH, POINTER_DEVICE_TYPE_TOUCH_PAD, input_pointerdevice.pointer_device_type, unifiedinputstack.pointer_device_type, winuser/POINTER_DEVICE_TYPE, winuser/POINTER_DEVICE_TYPE_EXTERNAL_PEN, winuser/POINTER_DEVICE_TYPE_INTEGRATED_PEN, winuser/POINTER_DEVICE_TYPE_MAX, winuser/POINTER_DEVICE_TYPE_TOUCH, winuser/POINTER_DEVICE_TYPE_TOUCH_PAD
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - POINTER_DEVICE_TYPE
product: Windows
targetos: Windows
req.typenames: POINTER_DEVICE_TYPE
req.redist: 
---

# POINTER_DEVICE_TYPE enumeration


## -description


Identifies the pointer device types.


## -enum-fields




### -field POINTER_DEVICE_TYPE_INTEGRATED_PEN

Direct pen digitizer (integrated into display).


### -field POINTER_DEVICE_TYPE_EXTERNAL_PEN

Indirect pen digitizer (not integrated into display).


### -field POINTER_DEVICE_TYPE_TOUCH

Touch digitizer.


### -field POINTER_DEVICE_TYPE_TOUCH_PAD

Touchpad digitizer (Windows 8.1 and later).


### -field POINTER_DEVICE_TYPE_MAX

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value. 


## -see-also




<a href="https://msdn.microsoft.com/39A3FB53-DFC9-4189-A05B-6E01DB0DF922">Enumerations</a>
 

 

