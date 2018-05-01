---
UID: NI:ntddkbd.IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION
title: IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION
author: windows-driver-content
description: The IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION request returns information about the mapping between scan codes and indicators.
old-location: hid\ioctl_keyboard_query_indicator_translation.htm
old-project: hid
ms.assetid: 84006453-cf73-44f2-ac8b-ea03382e113d
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION, IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION control code [Human Input Devices], hid.ioctl_keyboard_query_indicator_translation, kref_6d0fc5dc-e636-464a-a537-c3a39b8cba53.xml, ntddkbd/IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION
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
-	IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION IOCTL


## -description



     The IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION request returns information about the mapping between scan codes and indicators.   
    

Kbdclass copies the current stack location, sets the <b>MajorFunction</b> member of the new stack location to <a href="https://msdn.microsoft.com/library/windows/hardware/ff550766">IRP_MJ_INTERNAL_DEVICE_CONTROL</a>, and sends this request down the device stack.


## -ioctlparameters




### -input-buffer

The <b>Parameters.DeviceIoControl.InputBufferLength</b> member is set to zero or a value greater than or equal to the size, in bytes, of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542352">KEYBOARD_UNIT_ID_PARAMETER</a>. A value of zero specifies a default unit ID of zero.

The <b>AssociatedIrp.SystemBuffer </b>member points to a client-allocated buffer that is used to input and output information. On input, <b>AssociatedIrp.SystemBuffer</b> points to a KEYBOARD_UNIT_ID_PARAMETER structure. The client sets the <b>UnitId</b> member of the input structure.

The <b>Parameters.DeviceIoControl.OutputBufferLength</b> member specifies the size, in bytes, of a client-allocated output buffer, which must be greater than or equal to the size, in bytes, of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542334">KEYBOARD_INDICATOR_TRANSLATION</a> structure. (Note that this structure contains a device-specific array of members that map indicators to scan codes.)


### -input-buffer-length

A value greater than or equal to the size of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542334">KEYBOARD_INDICATOR_TRANSLATION</a> structure.


### -output-buffer

<b>AssociatedIrp.SystemBuffer</b> points to a client-allocated buffer that the lower-level drivers use to output a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542334">KEYBOARD_INDICATOR_TRANSLATION</a> structure.


### -output-buffer-length

 The size of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff542334">KEYBOARD_INDICATOR_TRANSLATION</a> structure.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

If the request is successful, the <b>Information</b> member is set to the number of bytes of translation data in the KEYBOARD_INDICATOR_TRANSLATION structure.

The <b>Status</b> member is set to one of the following values:




#### -STATUS_BUFFER_TOO_SMALL

The output buffer cannot hold the KEYBOARD_INDICATOR_TRANSLATION data.


#### -STATUS_INVALID_PARAMETER

The <b>UnitId</b> value is not valid.


#### -STATUS_NOT_SUPPORTED

The target device is associated with a subordinate class device.


#### -STATUS_SUCCESS

The request completed successfully.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541318">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541337">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541362">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542067">IOCTL_KEYBOARD_SET_INDICATORS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542076">IOCTL_KEYBOARD_SET_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542334">KEYBOARD_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542352">KEYBOARD_UNIT_ID_PARAMETER</a>
 

 

