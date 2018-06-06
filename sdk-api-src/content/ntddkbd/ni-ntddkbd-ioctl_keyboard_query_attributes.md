---
UID: NI:ntddkbd.IOCTL_KEYBOARD_QUERY_ATTRIBUTES
title: IOCTL_KEYBOARD_QUERY_ATTRIBUTES
author: windows-sdk-content
description: The IOCTL_KEYBOARD_QUERY_ATTRIBUTES request returns information about the keyboard attributes.
old-location: hid\ioctl_keyboard_query_attributes.htm
old-project: hid
ms.assetid: 6119ca39-f740-4c8a-a7f1-eb6f30624093
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: IOCTL_KEYBOARD_QUERY_ATTRIBUTES, IOCTL_KEYBOARD_QUERY_ATTRIBUTES control, IOCTL_KEYBOARD_QUERY_ATTRIBUTES control code [Human Input Devices], hid.ioctl_keyboard_query_attributes, kref_1522bb4a-6d24-4a25-a5fe-73343ff6c131.xml, ntddkbd/IOCTL_KEYBOARD_QUERY_ATTRIBUTES
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
 - IOCTL_KEYBOARD_QUERY_ATTRIBUTES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOCTL_KEYBOARD_QUERY_ATTRIBUTES IOCTL


## -description



     The IOCTL_KEYBOARD_QUERY_ATTRIBUTES request returns information about the keyboard attributes.
    

Kbdclass copies the current stack location, sets the <b>MajorFunction</b> member of the new stack location to <a href="https://msdn.microsoft.com/library/windows/hardware/ff550766">IRP_MJ_INTERNAL_DEVICE_CONTROL</a>, and sends this request down the device stack.

For more information about this request, see the description of this request in <a href="https://msdn.microsoft.com/5bbe69cb-361d-4d9a-b589-5ab7f59496a3">I8042prt Keyboard Internal Device Control Requests</a>.


## -ioctlparameters




### -input-buffer

The <b>Parameters.DeviceIoControl.InputBufferLength</b> member is set to zero or a value greater than or equal to the size, in bytes, of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542352">KEYBOARD_UNIT_ID_PARAMETER</a>. A value of zero specifies a default unit ID of zero.

The <b>AssociatedIrp.SystemBuffer</b> member points to a client-allocated buffer that is used to input and output information. On input, <b>AssociatedIrp.SystemBuffer</b> points to a KEYBOARD_UNIT_ID_PARAMETER structure. The client sets the <b>UnitId</b> member of the input structure.

The <b>Parameters.DeviceIoControl.OutputBufferLength</b> member specifies the size, in bytes, of the output buffer, which must be greater than or equal to the size, in bytes, of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542326">KEYBOARD_ATTRIBUTES</a> structure.


### -input-buffer-length




### -output-buffer

<b>AssociatedIrp.SystemBuffer</b> points to a client-allocated buffer that the lower-level drivers use to output a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542326">KEYBOARD_ATTRIBUTES</a> structure.


### -output-buffer-length

The size of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542326">KEYBOARD_ATTRIBUTES</a> structure.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

If the request is successful, the <b>Information</b> member is set to the size, in bytes, of a KEYBOARD_ATTRIBUTES structure, otherwise <b>Information</b> is set to zero.

The <b>Status</b> member is set to one of the following values:




#### -STATUS_BUFFER_TOO_SMALL

The value of <b>Parameters.DeviceIoControl.InputBufferLength </b>or <b>Parameters.DeviceIoControl.OutputBufferLength</b> is not valid.


#### -STATUS_INVALID_PARAMETER

The <b>UnitId </b>value is not valid.


#### -STATUS_SUCCESS

The request completed successfully.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541337">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541349">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541362">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542067">IOCTL_KEYBOARD_SET_INDICATORS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542076">IOCTL_KEYBOARD_SET_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542326">KEYBOARD_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542352">KEYBOARD_UNIT_ID_PARAMETER</a>
 

 

