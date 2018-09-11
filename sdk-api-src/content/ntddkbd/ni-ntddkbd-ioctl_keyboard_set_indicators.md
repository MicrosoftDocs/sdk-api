---
UID: NI:ntddkbd.IOCTL_KEYBOARD_SET_INDICATORS
title: IOCTL_KEYBOARD_SET_INDICATORS
author: windows-sdk-content
description: The IOCTL_KEYBOARD_SET_INDICATORS request sets the keyboard indicators.
old-location: hid\ioctl_keyboard_set_indicators.htm
tech.root: hid
ms.assetid: 25631717-8aee-4eac-8337-46b13aa714a4
ms.author: windowssdkdev
ms.date: 07/30/2018
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
 - IOCTL_KEYBOARD_SET_INDICATORS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_KEYBOARD_SET_INDICATORS IOCTL


## -description


The IOCTL_KEYBOARD_SET_INDICATORS request sets the keyboard indicators.
     

Kbdclass copies the current stack location, sets the <b>MajorFunction</b> member of the new stack location to <a href="https://msdn.microsoft.com/fb3d4534-9c6f-4956-b702-5752f9798600">IRP_MJ_INTERNAL_DEVICE_CONTROL</a>, and sends this request down the driver stack.

If there is a grandmaster device, Kbdclass normally sets the keyboard indicators of all the subordinate class devices to a global setting. This operation is controlled by the registry entry value <b>SendOutputToAllPorts</b> under the key <b>HKLM\Services\CurrentControlSet\Kbdclass\Parameters</b>. If <b>SendOutputToAllPorts</b> is nonzero, Kdbclass sets all subordinate class devices to a gobal setting. Otherwise, Kbdclass sets only the device whose unit ID is zero. 


## -ioctlparameters




### -input-buffer

The <b>Parameters.DeviceIoControl.InputBufferLength</b> member specifies the size, in bytes, of a <a href="https://msdn.microsoft.com/68c9d24a-c1c9-4ef6-904d-6aeb68cea32a">KEYBOARD_INDICATOR_PARAMETERS</a> structure.

The <b>AssociatedIrp.SystemBuffer</b> member points to a client-allocated KEYBOARD_INDICATOR_PARAMETERS structure. The client sets the <b>UnitId</b> and <b>LedFlags</b> members.


### -input-buffer-length

The size of a <a href="https://msdn.microsoft.com/68c9d24a-c1c9-4ef6-904d-6aeb68cea32a">KEYBOARD_INDICATOR_PARAMETERS</a> structure.


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




<a href="https://msdn.microsoft.com/6119ca39-f740-4c8a-a7f1-eb6f30624093">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/3d70b34c-e201-40fc-99dd-cd05bdeec5f8">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://msdn.microsoft.com/84006453-cf73-44f2-ac8b-ea03382e113d">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/0c19670b-0440-4a7a-ad87-a97d3da28e74">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/27c538dd-19e2-4b5a-9605-0efb0f78e008">IOCTL_KEYBOARD_SET_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/68c9d24a-c1c9-4ef6-904d-6aeb68cea32a">KEYBOARD_INDICATOR_PARAMETERS</a>
 

 

