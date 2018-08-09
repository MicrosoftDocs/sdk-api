---
UID: NI:ntddkbd.IOCTL_KEYBOARD_QUERY_TYPEMATIC
title: IOCTL_KEYBOARD_QUERY_TYPEMATIC
author: windows-sdk-content
description: The IOCTL_KEYBOARD_QUERY_TYPEMATIC request returns the typematic settings.
old-location: hid\ioctl_keyboard_query_typematic.htm
old-project: hid
ms.assetid: 0c19670b-0440-4a7a-ad87-a97d3da28e74
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IOCTL_KEYBOARD_QUERY_TYPEMATIC, IOCTL_KEYBOARD_QUERY_TYPEMATIC  control, IOCTL_KEYBOARD_QUERY_TYPEMATIC control code [Human Input Devices], hid.ioctl_keyboard_query_typematic, kref_6b6b2db2-e848-47bb-8972-afde72c9be36.xml, ntddkbd/IOCTL_KEYBOARD_QUERY_TYPEMATIC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: ioctl
req.header: ntddkbd.h
req.include-header: Ntddkbd.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SERVICE_TYPE_VALUE_ABSW (Unicode) and SERVICE_TYPE_VALUE_ABSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SERVICE_TYPE_VALUE_ABSW, *PSERVICE_TYPE_VALUE_ABSW, *LPSERVICE_TYPE_VALUE_ABSW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddkbd.h
api_name:
 - IOCTL_KEYBOARD_QUERY_TYPEMATIC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOCTL_KEYBOARD_QUERY_TYPEMATIC IOCTL


## -description


The IOCTL_KEYBOARD_QUERY_TYPEMATIC request returns the typematic settings.
     
    

Kbdclass copies the current stack location, sets the <b>MajorFunction</b> member of the new stack location to <a href="https://msdn.microsoft.com/library/windows/hardware/ff550766">IRP_MJ_INTERNAL_DEVICE_CONTROL</a>, and sends this request down the device stack.


## -ioctlparameters




### -input-buffer

The <b>Parameters.DeviceIoControl.InputBufferLength</b> member is set to zero or a value greater than or equal to the size, in bytes, of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542352">KEYBOARD_UNIT_ID_PARAMETER</a>. A value of zero specifies a default unit ID of zero.

The <b>AssociatedIrp.SystemBuffer </b>member points to a client-allocated buffer that is used to input and output information. On input, <b>AssociatedIrp.SystemBuffer</b> points to a KEYBOARD_UNIT_ID_PARAMETER structure. The client sets the <b>UnitId</b> member of the input structure.


### -input-buffer-length

The size of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542352">KEYBOARD_UNIT_ID_PARAMETER</a> structure.


### -output-buffer

<b>AssociatedIrp.SystemBuffer</b> points to the client-allocated buffer that the lower-level drivers use to output a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542346">KEYBOARD_TYPEMATIC_PARAMETERS</a> structure.


### -output-buffer-length

The size of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542346">KEYBOARD_TYPEMATIC_PARAMETERS</a> structure.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

If the request is successful, the <b>Information</b> member is set to the number of bytes of a KEYBOARD_TYPEMATIC_PARAMETERS structure.

The <b>Status</b> member is set to one of the following values:








#### -STATUS_SUCCESS

The request completed successfully.


#### -STATUS_INVALID_PARAMETER

The <b>UnitId</b> value is not valid.


#### -STATUS_BUFFER_TOO_SMALL

The output buffer cannot hold the KEYBOARD_TYPEMATIC_PARAMETERS data.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541318">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541337">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541349">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542067">IOCTL_KEYBOARD_SET_INDICATORS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542076">IOCTL_KEYBOARD_SET_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542346">KEYBOARD_TYPEMATIC_PARAMETERS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542352">KEYBOARD_UNIT_ID_PARAMETER</a>
 

 

