---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IOCTL_MOUSE_QUERY_ATTRIBUTES IOCTL


## -description


The IOCTL_MOUSE_QUERY_ATTRIBUTES request returns information about the mouse attributes.

Mouclass copies the current stack location, sets the <b>MajorFunction</b> member of the new stack location to <a href="https://msdn.microsoft.com/library/windows/hardware/ff550766">IRP_MJ_INTERNAL_DEVICE_CONTROL</a>, and sends this request down the device stack.

For more information about this request, see <a href="https://msdn.microsoft.com/29427f60-b584-48ef-ba3c-a83bc845b51e">I8042prt Mouse Internal Device Control Requests</a>.


## -ioctlparameters




### -input-buffer

The <b>Parameters.DeviceIoControl.InputBufferLength</b> member is set to zero or a value greater than or equal to the size, in bytes, of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542409">MOUSE_UNIT_ID_PARAMETER</a>. A value of zero specifies a default unit ID of zero.

The <b>AssociatedIrp.SystemBuffer </b>member points to a client-allocated buffer that is used to input and output information. On input, <b>AssociatedIrp.SystemBuffer</b> points to a MOUSE_UNIT_ID_PARAMETER structure. The client sets the <b>UnitId</b> member of the input structure.

The <b>Parameters.DeviceIoControl.OutputBufferLength</b> member specifies the size, in bytes, of an output buffer, which must be greater than or equal to the size in bytes of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542398">MOUSE_ATTRIBUTES</a> structure.


### -input-buffer-length

The size of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542409">MOUSE_UNIT_ID_PARAMETER</a> structure.


### -output-buffer

<b>AssociatedIrp.SystemBuffer</b> points to the client-allocated buffer that the lower-level drivers use to output a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542398">MOUSE_ATTRIBUTES</a> structure.


### -output-buffer-length

The size of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542398">MOUSE_ATTRIBUTES</a> structure.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

The <b>Information</b> member is set to the number of bytes of attribute data that are returned if the request is successful. 

The <b>Status</b> member is set to one of the following values:




#### -STATUS_BUFFER_TOO_SMALL

The <b>Parameters.DeviceIoControl.InputBufferLength </b>value is greater than zero but less than the size, in bytes, of a MOUSE_UNIT_ID_PARAMETER structure.


#### -STATUS_INVALID_PARAMETER

The <b>UnitId </b>value is invalid.


#### -STATUS_NOT_SUPPORTED

The target device is associated with a subordinate class device.


#### -STATUS_SUCCESS

The request completed successfully.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff542398">MOUSE_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542409">MOUSE_UNIT_ID_PARAMETER</a>
 

 

