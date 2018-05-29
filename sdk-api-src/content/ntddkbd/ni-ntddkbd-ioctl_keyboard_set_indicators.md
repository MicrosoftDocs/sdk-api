---
UID: NI:ntddkbd.IOCTL_KEYBOARD_SET_INDICATORS
title: IOCTL_KEYBOARD_SET_INDICATORS
author: windows-sdk-content
description: The IOCTL_KEYBOARD_SET_INDICATORS request sets the keyboard indicators.
old-location: hid\ioctl_keyboard_set_indicators.htm
old-project: hid
ms.assetid: 25631717-8aee-4eac-8337-46b13aa714a4
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: IOCTL_KEYBOARD_SET_INDICATORS, IOCTL_KEYBOARD_SET_INDICATORS control, IOCTL_KEYBOARD_SET_INDICATORS control code [Human Input Devices], hid.ioctl_keyboard_set_indicators, kref_de568d6c-e4d3-494b-a4fc-c5537e7b59b9.xml, ntddkbd/IOCTL_KEYBOARD_SET_INDICATORS
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
req.typenames: SERVICE_TYPE_VALUE_ABSW, *PSERVICE_TYPE_VALUE_ABSW, *LPSERVICE_TYPE_VALUE_ABSW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ntddkbd.h
api_name:
-	IOCTL_KEYBOARD_SET_INDICATORS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

