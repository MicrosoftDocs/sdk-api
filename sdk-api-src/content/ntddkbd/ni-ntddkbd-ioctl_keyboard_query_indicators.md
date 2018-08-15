---
UID: NI:ntddkbd.IOCTL_KEYBOARD_QUERY_INDICATORS
title: IOCTL_KEYBOARD_QUERY_INDICATORS
author: windows-sdk-content
description: The IOCTL_KEYBOARD_QUERY_INDICATORS request returns information about the keyboard indicators.
old-location: hid\ioctl_keyboard_query_indicators.htm
old-project: hid
ms.assetid: 3d70b34c-e201-40fc-99dd-cd05bdeec5f8
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IOCTL_KEYBOARD_QUERY_INDICATORS, IOCTL_KEYBOARD_QUERY_INDICATORS control, IOCTL_KEYBOARD_QUERY_INDICATORS control code [Human Input Devices], hid.ioctl_keyboard_query_indicators, kref_41aef51b-c9f1-4549-b67a-cb7a3a9424c4.xml, ntddkbd/IOCTL_KEYBOARD_QUERY_INDICATORS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: ioctl
req.header: ntddkbd.h
req.include-header: Ntddkbd.h
req.redist: 
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
 - IOCTL_KEYBOARD_QUERY_INDICATORS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOCTL_KEYBOARD_QUERY_INDICATORS IOCTL


## -description


The IOCTL_KEYBOARD_QUERY_INDICATORS request returns information about the keyboard indicators.
     
    

Kbdclass copies the current stack location, sets the <b>MajorFunction</b> member of the new stack location to <a href="https://msdn.microsoft.com/fb3d4534-9c6f-4956-b702-5752f9798600">IRP_MJ_INTERNAL_DEVICE_CONTROL</a>, and sends this request down the device stack.


## -ioctlparameters




### -input-buffer

The <b>Parameters.DeviceIoControl.InputBufferLength</b> member is set to zero or a value greater than or equal to the size, in bytes, of a <a href="https://msdn.microsoft.com/fd47b0ab-b66b-49a0-8302-2c45399d9963">KEYBOARD_UNIT_ID_PARAMETER</a>. A value of zero specifies a default unit ID of zero.

The <b>AssociatedIrp.SystemBuffer </b>member points to a client-allocated buffer that is used to input and output information. On input, <b>AssociatedIrp.SystemBuffer</b> points to a KEYBOARD_UNIT_ID_PARAMETER structure. The client sets the <b>UnitId</b> member of the input structure.

The <b>Parameters.DeviceIoControl.OutputBufferLength</b> member specifies the size, in bytes, of the output buffer, which must be greater than or equal to the size, in bytes, of a <a href="https://msdn.microsoft.com/68c9d24a-c1c9-4ef6-904d-6aeb68cea32a">KEYBOARD_INDICATOR_PARAMETERS</a> structure.


### -input-buffer-length

The size of a <a href="https://msdn.microsoft.com/fd47b0ab-b66b-49a0-8302-2c45399d9963">KEYBOARD_UNIT_ID_PARAMETER</a> structure.


### -output-buffer

<b>AssociatedIrp.SystemBuffer</b> points to a client-allocated buffer that the lower-level drivers use to output a <a href="https://msdn.microsoft.com/68c9d24a-c1c9-4ef6-904d-6aeb68cea32a">KEYBOARD_INDICATOR_PARAMETERS</a> structure.


### -output-buffer-length

The size of  a <a href="https://msdn.microsoft.com/68c9d24a-c1c9-4ef6-904d-6aeb68cea32a">KEYBOARD_INDICATOR_PARAMETERS</a> structure.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

If the request is successful, the <b>Information</b> member is set to the size, in bytes, of a KEYBOARD_INDICATOR_PARAMETERS structure.

The <b>Status</b> member is set to one the following values:




#### -STATUS_BUFFER_TOO_SMALL

The output buffer cannot hold the KEYBOARD_INDICATOR_PARAMETERS structure.


#### -STATUS_INVALID_PARAMETER

The <b>UnitId</b> value is not valid.


#### -STATUS_SUCCESS

The request completed successfully.


## -see-also




<a href="https://msdn.microsoft.com/6119ca39-f740-4c8a-a7f1-eb6f30624093">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/84006453-cf73-44f2-ac8b-ea03382e113d">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/0c19670b-0440-4a7a-ad87-a97d3da28e74">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/25631717-8aee-4eac-8337-46b13aa714a4">IOCTL_KEYBOARD_SET_INDICATORS</a>



<a href="https://msdn.microsoft.com/27c538dd-19e2-4b5a-9605-0efb0f78e008">IOCTL_KEYBOARD_SET_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/68c9d24a-c1c9-4ef6-904d-6aeb68cea32a">KEYBOARD_INDICATOR_PARAMETERS</a>



<a href="https://msdn.microsoft.com/fd47b0ab-b66b-49a0-8302-2c45399d9963">KEYBOARD_UNIT_ID_PARAMETER</a>
 

 

