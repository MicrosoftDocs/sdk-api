---
UID: NI:ntddkbd.IOCTL_KEYBOARD_QUERY_ATTRIBUTES
title: IOCTL_KEYBOARD_QUERY_ATTRIBUTES
author: windows-sdk-content
description: The IOCTL_KEYBOARD_QUERY_ATTRIBUTES request returns information about the keyboard attributes.
old-location: hid\ioctl_keyboard_query_attributes.htm
tech.root: hid
ms.assetid: 6119ca39-f740-4c8a-a7f1-eb6f30624093
ms.author: windowssdkdev
ms.date: 08/29/2018
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
 - ntddkbd.h
api_name:
 - IOCTL_KEYBOARD_QUERY_ATTRIBUTES
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_KEYBOARD_QUERY_ATTRIBUTES IOCTL


## -description


The IOCTL_KEYBOARD_QUERY_ATTRIBUTES request returns information about the keyboard attributes.
    

Kbdclass copies the current stack location, sets the <b>MajorFunction</b> member of the new stack location to <a href="https://msdn.microsoft.com/fb3d4534-9c6f-4956-b702-5752f9798600">IRP_MJ_INTERNAL_DEVICE_CONTROL</a>, and sends this request down the device stack.

For more information about this request, see the description of this request in <a href="https://msdn.microsoft.com/5bbe69cb-361d-4d9a-b589-5ab7f59496a3">I8042prt Keyboard Internal Device Control Requests</a>.


## -ioctlparameters




### -input-buffer

The <b>Parameters.DeviceIoControl.InputBufferLength</b> member is set to zero or a value greater than or equal to the size, in bytes, of a <a href="https://msdn.microsoft.com/fd47b0ab-b66b-49a0-8302-2c45399d9963">KEYBOARD_UNIT_ID_PARAMETER</a>. A value of zero specifies a default unit ID of zero.

The <b>AssociatedIrp.SystemBuffer</b> member points to a client-allocated buffer that is used to input and output information. On input, <b>AssociatedIrp.SystemBuffer</b> points to a KEYBOARD_UNIT_ID_PARAMETER structure. The client sets the <b>UnitId</b> member of the input structure.

The <b>Parameters.DeviceIoControl.OutputBufferLength</b> member specifies the size, in bytes, of the output buffer, which must be greater than or equal to the size, in bytes, of a <a href="https://msdn.microsoft.com/060e93de-b84e-4755-a5f8-cbc52d900310">KEYBOARD_ATTRIBUTES</a> structure.


### -input-buffer-length




### -output-buffer

<b>AssociatedIrp.SystemBuffer</b> points to a client-allocated buffer that the lower-level drivers use to output a <a href="https://msdn.microsoft.com/060e93de-b84e-4755-a5f8-cbc52d900310">KEYBOARD_ATTRIBUTES</a> structure.


### -output-buffer-length

The size of a <a href="https://msdn.microsoft.com/060e93de-b84e-4755-a5f8-cbc52d900310">KEYBOARD_ATTRIBUTES</a> structure.


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




<a href="https://msdn.microsoft.com/3d70b34c-e201-40fc-99dd-cd05bdeec5f8">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://msdn.microsoft.com/84006453-cf73-44f2-ac8b-ea03382e113d">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/0c19670b-0440-4a7a-ad87-a97d3da28e74">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/25631717-8aee-4eac-8337-46b13aa714a4">IOCTL_KEYBOARD_SET_INDICATORS</a>



<a href="https://msdn.microsoft.com/27c538dd-19e2-4b5a-9605-0efb0f78e008">IOCTL_KEYBOARD_SET_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/060e93de-b84e-4755-a5f8-cbc52d900310">KEYBOARD_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/fd47b0ab-b66b-49a0-8302-2c45399d9963">KEYBOARD_UNIT_ID_PARAMETER</a>
 

 

