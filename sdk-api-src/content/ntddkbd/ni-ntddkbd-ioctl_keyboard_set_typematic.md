---
UID: NI:ntddkbd.IOCTL_KEYBOARD_SET_TYPEMATIC
title: IOCTL_KEYBOARD_SET_TYPEMATIC
author: windows-driver-content
description: The IOCTL_KEYBOARD_SET_TYPEMATIC request sets the typematic parameters.
old-location: hid\ioctl_keyboard_set_typematic.htm
old-project: hid
ms.assetid: 27c538dd-19e2-4b5a-9605-0efb0f78e008
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IOCTL_KEYBOARD_SET_TYPEMATIC, IOCTL_KEYBOARD_SET_TYPEMATIC control, IOCTL_KEYBOARD_SET_TYPEMATIC control code [Human Input Devices], hid.ioctl_keyboard_set_typematic, kref_1ef2189f-4cae-4a7d-b91d-9725a6ea6cba.xml, ntddkbd/IOCTL_KEYBOARD_SET_TYPEMATIC
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SERVICE_TYPE_VALUE_ABSW, *PSERVICE_TYPE_VALUE_ABSW, *LPSERVICE_TYPE_VALUE_ABSW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ntddkbd.h
api_name:
-	IOCTL_KEYBOARD_SET_TYPEMATIC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOCTL_KEYBOARD_SET_TYPEMATIC IOCTL


## -description



     The IOCTL_KEYBOARD_SET_TYPEMATIC request sets the typematic parameters.
    

Kbdclass copies the current stack location, sets the <b>MajorFunction</b> member of the new stack location to <a href="https://msdn.microsoft.com/library/windows/hardware/ff550766">IRP_MJ_INTERNAL_DEVICE_CONTROL</a>, and sends this request down the device stack.

Note that if there is a grandmaster device, Kbdclass normally sets the typematic settings of all the subordinate class devices to the same global setting. This operation is controlled by the grandmaster's registry entry value <b>SendOutputToAllPorts</b> under the key <b>HKLM\Services\CurrentControlSet\Kbdclass\Parameters</b>. 


## -ioctlparameters




### -input-buffer

The <b>Parameters.DeviceIoControl.InputBufferLength</b> member is set to a value greater than or equal to the size, in bytes, of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542346">KEYBOARD_TYPEMATIC_PARAMETERS</a> structure.

The <b>AssociatedIrp.SystemBuffer</b> member points to a client-allocated KEYBOARD_TYPEMATIC_PARAMETERS structure. The client sets the <b>UnitId</b>, <b>Rate</b>, and <b>Delay</b> member values. 


### -input-buffer-length

The size of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542346">KEYBOARD_TYPEMATIC_PARAMETERS</a> structure.


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

<b>Parameters.DeviceIoControl.InputBufferLength</b> is less than the size, in bytes, of a KEYBOARD_TYPEMATIC_PARAMETERS structure.


#### -STATUS_INVALID_PARAMETER

The <b>UnitId</b> value is invalid.


#### -STATUS_IO_TIMEOUT

The operation timed out.


#### -STATUS_SUCCESS

The request completed successfully.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541318">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541337">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541349">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541362">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542067">IOCTL_KEYBOARD_SET_INDICATORS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542346">KEYBOARD_TYPEMATIC_PARAMETERS</a>
 

 

