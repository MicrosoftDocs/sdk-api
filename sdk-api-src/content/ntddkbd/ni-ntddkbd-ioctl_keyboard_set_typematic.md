---
UID: NI:ntddkbd.IOCTL_KEYBOARD_SET_TYPEMATIC
title: IOCTL_KEYBOARD_SET_TYPEMATIC
author: windows-sdk-content
description: The IOCTL_KEYBOARD_SET_TYPEMATIC request sets the typematic parameters.
old-location: hid\ioctl_keyboard_set_typematic.htm
tech.root: hid
ms.assetid: 27c538dd-19e2-4b5a-9605-0efb0f78e008
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IOCTL_KEYBOARD_SET_TYPEMATIC, IOCTL_KEYBOARD_SET_TYPEMATIC control, IOCTL_KEYBOARD_SET_TYPEMATIC control code [Human Input Devices], hid.ioctl_keyboard_set_typematic, kref_1ef2189f-4cae-4a7d-b91d-9725a6ea6cba.xml, ntddkbd/IOCTL_KEYBOARD_SET_TYPEMATIC
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
 - IOCTL_KEYBOARD_SET_TYPEMATIC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_KEYBOARD_SET_TYPEMATIC IOCTL


## -description


The IOCTL_KEYBOARD_SET_TYPEMATIC request sets the typematic parameters.
    

Kbdclass copies the current stack location, sets the <b>MajorFunction</b> member of the new stack location to <a href="https://msdn.microsoft.com/fb3d4534-9c6f-4956-b702-5752f9798600">IRP_MJ_INTERNAL_DEVICE_CONTROL</a>, and sends this request down the device stack.

Note that if there is a grandmaster device, Kbdclass normally sets the typematic settings of all the subordinate class devices to the same global setting. This operation is controlled by the grandmaster's registry entry value <b>SendOutputToAllPorts</b> under the key <b>HKLM\Services\CurrentControlSet\Kbdclass\Parameters</b>. 


## -ioctlparameters




### -input-buffer

The <b>Parameters.DeviceIoControl.InputBufferLength</b> member is set to a value greater than or equal to the size, in bytes, of a <a href="https://msdn.microsoft.com/4bbf1699-1ba9-4569-97ac-156a91405586">KEYBOARD_TYPEMATIC_PARAMETERS</a> structure.

The <b>AssociatedIrp.SystemBuffer</b> member points to a client-allocated KEYBOARD_TYPEMATIC_PARAMETERS structure. The client sets the <b>UnitId</b>, <b>Rate</b>, and <b>Delay</b> member values. 


### -input-buffer-length

The size of a <a href="https://msdn.microsoft.com/4bbf1699-1ba9-4569-97ac-156a91405586">KEYBOARD_TYPEMATIC_PARAMETERS</a> structure.


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




<a href="https://msdn.microsoft.com/6119ca39-f740-4c8a-a7f1-eb6f30624093">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/3d70b34c-e201-40fc-99dd-cd05bdeec5f8">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://msdn.microsoft.com/84006453-cf73-44f2-ac8b-ea03382e113d">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/0c19670b-0440-4a7a-ad87-a97d3da28e74">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/25631717-8aee-4eac-8337-46b13aa714a4">IOCTL_KEYBOARD_SET_INDICATORS</a>



<a href="https://msdn.microsoft.com/4bbf1699-1ba9-4569-97ac-156a91405586">KEYBOARD_TYPEMATIC_PARAMETERS</a>
 

 

