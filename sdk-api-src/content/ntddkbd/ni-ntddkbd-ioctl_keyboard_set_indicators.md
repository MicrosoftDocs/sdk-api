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

# IOCTL_KEYBOARD_SET_INDICATORS IOCTL


## -description



     The IOCTL_KEYBOARD_SET_INDICATORS request sets the keyboard indicators.
     

Kbdclass copies the current stack location, sets the <b>MajorFunction</b> member of the new stack location to <a href="https://msdn.microsoft.com/library/windows/hardware/ff550766">IRP_MJ_INTERNAL_DEVICE_CONTROL</a>, and sends this request down the driver stack.

If there is a grandmaster device, Kbdclass normally sets the keyboard indicators of all the subordinate class devices to a global setting. This operation is controlled by the registry entry value <b>SendOutputToAllPorts</b> under the key <b>HKLM\Services\CurrentControlSet\Kbdclass\Parameters</b>. If <b>SendOutputToAllPorts</b> is nonzero, Kdbclass sets all subordinate class devices to a gobal setting. Otherwise, Kbdclass sets only the device whose unit ID is zero. 


## -ioctlparameters




### -input-buffer

The <b>Parameters.DeviceIoControl.InputBufferLength</b> member specifies the size, in bytes, of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542331">KEYBOARD_INDICATOR_PARAMETERS</a> structure.

The <b>AssociatedIrp.SystemBuffer</b> member points to a client-allocated KEYBOARD_INDICATOR_PARAMETERS structure. The client sets the <b>UnitId</b> and <b>LedFlags</b> members.


### -input-buffer-length

The size of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542331">KEYBOARD_INDICATOR_PARAMETERS</a> structure.


### -output-buffer


       None.


### -output-buffer-length

None.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

The <b>Information</b> member is set to zero. 

The <b>Status</b> member is set to one of the following values:




#### -STATUS_BUFFER_TOO_SMALL

The value of <b>Parameters.DeviceIoControl.InputBufferLength</b> is less than the size, in bytes, of a KEYBOARD_INDICATOR_PARAMETERS structure.


#### -STATUS_INVALID_PARAMETER

The <b>UnitId</b> value is invalid.


#### -STATUS_IO_TIMEOUT

The requested operation timed out on the device.


#### -STATUS_SUCCESS

The request completed successfully.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541318">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541337">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541349">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541362">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542076">IOCTL_KEYBOARD_SET_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542331">KEYBOARD_INDICATOR_PARAMETERS</a>
 

 

