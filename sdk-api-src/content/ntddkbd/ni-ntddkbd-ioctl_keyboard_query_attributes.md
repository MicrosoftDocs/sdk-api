---
UID: NI:ntddkbd.IOCTL_KEYBOARD_QUERY_ATTRIBUTES
title: IOCTL_KEYBOARD_QUERY_ATTRIBUTES (ntddkbd.h)
description: The IOCTL_KEYBOARD_QUERY_ATTRIBUTES request returns information about the keyboard attributes.
helpviewer_keywords: ["IOCTL_KEYBOARD_QUERY_ATTRIBUTES","IOCTL_KEYBOARD_QUERY_ATTRIBUTES control","IOCTL_KEYBOARD_QUERY_ATTRIBUTES control code [Human Input Devices]","hid.ioctl_keyboard_query_attributes2","i8042ref_51ea405d-a67d-4074-9e29-a307c9681196.xml","ntddkbd/IOCTL_KEYBOARD_QUERY_ATTRIBUTES"]
old-location: hid\ioctl_keyboard_query_attributes2.htm
tech.root: hid
ms.assetid: ebf0f275-dbf6-4538-bd90-40ba47a8bfc0
ms.date: 12/05/2018
ms.keywords: IOCTL_KEYBOARD_QUERY_ATTRIBUTES, IOCTL_KEYBOARD_QUERY_ATTRIBUTES control, IOCTL_KEYBOARD_QUERY_ATTRIBUTES control code [Human Input Devices], hid.ioctl_keyboard_query_attributes2, i8042ref_51ea405d-a67d-4074-9e29-a307c9681196.xml, ntddkbd/IOCTL_KEYBOARD_QUERY_ATTRIBUTES
f1_keywords:
- ntddkbd/IOCTL_KEYBOARD_QUERY_ATTRIBUTES
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOCTL_KEYBOARD_QUERY_ATTRIBUTES IOCTL


## -description


The IOCTL_KEYBOARD_QUERY_ATTRIBUTES request returns information about the keyboard attributes.


## -ioctlparameters




### -input-buffer

<b>Parameters.DeviceIoControl.OutputBufferLength</b> is set to a value greater than or equal to the size, in bytes, of a <a href="https://docs.microsoft.com/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_attributes">KEYBOARD_ATTRIBUTES</a> structure.


### -input-buffer-length

The size of a <a href="https://docs.microsoft.com/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_attributes">KEYBOARD_ATTRIBUTES</a> structure.


### -output-buffer

<b>AssociatedIrp.SystemBuffer</b> points to a client-allocated buffer that I8042prt uses to output a <a href="https://docs.microsoft.com/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_attributes">KEYBOARD_ATTRIBUTES</a> structure.


### -output-buffer-length

The size of a <a href="https://docs.microsoft.com/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_attributes">KEYBOARD_ATTRIBUTES</a> structure.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

If the request is successful, the <b>Information</b> member is set to the size, in bytes, of a KEYBOARD_ATTRIBUTES structure. Otherwise the <b>Information</b> member is set to zero.

The <b>Status</b> member is set to one of the following values:




#### -STATUS_BUFFER_TOO_SMALL

<b>Parameters.DeviceIoControl.OutputBufferLength</b> is less than the size, in bytes, of a KEYBOARD_ATTRIBUTES structure.


#### -STATUS_SUCCESS

The request completed successfully.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_indicators">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_indicator_translation">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_typematic">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_attributes">KEYBOARD_ATTRIBUTES</a>
 

 

