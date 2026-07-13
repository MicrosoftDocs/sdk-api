---
UID: NI:ntddkbd.IOCTL_KEYBOARD_QUERY_TYPEMATIC
title: IOCTL_KEYBOARD_QUERY_TYPEMATIC (ntddkbd.h)
description: The IOCTL_KEYBOARD_QUERY_TYPEMATIC request returns the keyboard typematic settings.
helpviewer_keywords: ["IOCTL_KEYBOARD_QUERY_TYPEMATIC","IOCTL_KEYBOARD_QUERY_TYPEMATIC control","IOCTL_KEYBOARD_QUERY_TYPEMATIC control code [Human Input Devices]","hid.ioctl_keyboard_query_typematic2","i8042ref_4aaa5c7a-3a1e-4f50-950f-3e03c0a0c034.xml","ntddkbd/IOCTL_KEYBOARD_QUERY_TYPEMATIC"]
old-location: hid\ioctl_keyboard_query_typematic2.htm
tech.root: hid
ms.assetid: c27c6bfb-026d-43ab-b394-9bba7df01511
ms.date: 12/05/2018
ms.keywords: IOCTL_KEYBOARD_QUERY_TYPEMATIC, IOCTL_KEYBOARD_QUERY_TYPEMATIC control, IOCTL_KEYBOARD_QUERY_TYPEMATIC control code [Human Input Devices], hid.ioctl_keyboard_query_typematic2, i8042ref_4aaa5c7a-3a1e-4f50-950f-3e03c0a0c034.xml, ntddkbd/IOCTL_KEYBOARD_QUERY_TYPEMATIC
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOCTL_KEYBOARD_QUERY_TYPEMATIC
 - ntddkbd/IOCTL_KEYBOARD_QUERY_TYPEMATIC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddkbd.h
api_name:
 - IOCTL_KEYBOARD_QUERY_TYPEMATIC
---

# IOCTL_KEYBOARD_QUERY_TYPEMATIC IOCTL


## -description

The IOCTL_KEYBOARD_QUERY_TYPEMATIC request returns the keyboard typematic settings.

## -ioctlparameters

### -input-buffer

<b>Parameters.DeviceIoControl.OutputBufferLength</b> is set to a value greater than or equal to the size, in bytes, of a <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_typematic_parameters">KEYBOARD_TYPEMATIC_PARAMETERS</a> structure.

### -input-buffer-length

The size of a <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_typematic_parameters">KEYBOARD_TYPEMATIC_PARAMETERS</a> structure.

### -output-buffer

<b>AssociatedIrp.SystemBuffer</b> points to a client-allocated output buffer that I8042prt uses to output a <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_typematic_parameters">KEYBOARD_TYPEMATIC_PARAMETERS</a> structure.

### -output-buffer-length

The size of a <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_typematic_parameters">KEYBOARD_TYPEMATIC_PARAMETERS</a> structure.

### -in-out-buffer


### -inout-buffer-length


### -status-block

If the request is successful, the <b>Information</b> member is set to the size, in bytes, of a KEYBOARD_TYPEMATIC_PARAMETERS structure. Otherwise, <b>Information</b> is set to zero.

The <b>Status</b> member is set to one of the following values:

## -STATUS_BUFFER_TOO_SMALL

<b>Parameters.DeviceIoControl.OutputBufferLength</b> is less than the size, in bytes, of a KEYBOARD_TYPEMATIC_PARAMETERS structure.

## -STATUS_SUCCESS

The request completed successfully.

## -see-also

<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_attributes">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_indicators">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_indicator_translation">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_typematic_parameters">KEYBOARD_TYPEMATIC_PARAMETERS</a>