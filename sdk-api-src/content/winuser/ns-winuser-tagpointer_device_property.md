---
UID: NS:winuser.tagPOINTER_DEVICE_PROPERTY
title: tagPOINTER_DEVICE_PROPERTY
author: windows-sdk-content
description: Contains device properties (Human Interface Device (HID) global items that correspond to HID usages).
old-location: input_pointerdevice\pointer_device_property.htm
old-project: Input_PointerDevice
ms.assetid: 2c96379e-7c9f-440c-a98b-bda38bacd33f
ms.author: windowssdkdev
ms.date: 03/26/2018
ms.keywords: POINTER_DEVICE_PROPERTY, POINTER_DEVICE_PROPERTY structure, input_pointerdevice.pointer_device_property, tagPOINTER_DEVICE_PROPERTY, unifiedinputstack.pointer_device_property, winuser/POINTER_DEVICE_PROPERTY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: POINTER_DEVICE_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - POINTER_DEVICE_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagPOINTER_DEVICE_PROPERTY structure


## -description


Contains device properties (Human Interface Device (HID) global items that correspond to HID usages).


## -struct-fields




### -field logicalMin

The minimum value that the device can report for this property.


### -field logicalMax

The maximum value that the device can report for this property.


### -field physicalMin

The physical minimum  in Himetric.


### -field physicalMax

The physical maximum in Himetric.


### -field unit

The unit.


### -field unitExponent

The exponent.


### -field usagePageId

The usage page for the property, as documented in the HID specification.


### -field usageId

The usage  of  the property, as documented in the HID specification.


## -remarks



Developers can use this function to determine the properties that a device supports beyond the standard ones that are delivered through <a href="https://msdn.microsoft.com/BDF74777-101F-4089-94C1-5C28520CAD1A">Pointer Input Messages and Notifications</a>. The properties map directly to HID usages.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

