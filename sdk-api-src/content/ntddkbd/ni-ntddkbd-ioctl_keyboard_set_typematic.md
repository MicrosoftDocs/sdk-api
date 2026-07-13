---
UID: NI:ntddkbd.IOCTL_KEYBOARD_SET_TYPEMATIC
title: IOCTL_KEYBOARD_SET_TYPEMATIC (ntddkbd.h)
description: The IOCTL_KEYBOARD_SET_TYPEMATIC request sets the keyboard typematic settings.
helpviewer_keywords: ["IOCTL_KEYBOARD_SET_TYPEMATIC","IOCTL_KEYBOARD_SET_TYPEMATIC control","IOCTL_KEYBOARD_SET_TYPEMATIC control code [Human Input Devices]","hid.ioctl_keyboard_set_typematic2","i8042ref_1df6c763-6fbd-4a76-810a-7b0e6f624e9f.xml","ntddkbd/IOCTL_KEYBOARD_SET_TYPEMATIC"]
old-location: hid\ioctl_keyboard_set_typematic2.htm
tech.root: hid
ms.assetid: bcd2c72a-b1fd-4df4-8f65-0fe32eab00ef
ms.date: 12/05/2018
ms.keywords: IOCTL_KEYBOARD_SET_TYPEMATIC, IOCTL_KEYBOARD_SET_TYPEMATIC control, IOCTL_KEYBOARD_SET_TYPEMATIC control code [Human Input Devices], hid.ioctl_keyboard_set_typematic2, i8042ref_1df6c763-6fbd-4a76-810a-7b0e6f624e9f.xml, ntddkbd/IOCTL_KEYBOARD_SET_TYPEMATIC
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
 - IOCTL_KEYBOARD_SET_TYPEMATIC
 - ntddkbd/IOCTL_KEYBOARD_SET_TYPEMATIC
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
 - IOCTL_KEYBOARD_SET_TYPEMATIC
---

# IOCTL_KEYBOARD_SET_TYPEMATIC IOCTL


## -description

The IOCTL_KEYBOARD_SET_TYPEMATIC request sets the keyboard typematic settings.

## -ioctlparameters

### -input-buffer

<b>AssociatedIrp.SystemBuffer</b> points to a client-allocated buffer to input a <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_typematic_parameters">KEYBOARD_TYPEMATIC_PARAMETERS</a> structure. The client sets the typematic parameters in this structure.

<b>Parameters.DeviceIoControl.InputBufferLength</b> is set to a value greater than or equal to the size, in bytes, of a <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_typematic_parameters">KEYBOARD_TYPEMATIC_PARAMETERS</a> structure.

### -input-buffer-length

The size of a <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_typematic_parameters">KEYBOARD_TYPEMATIC_PARAMETERS</a> structure.

### -output-buffer

None.

### -output-buffer-length

None.

### -in-out-buffer


### -inout-buffer-length


### -status-block

The <b>Information</b> member is set to zero.

The <b>Status</b> member is set to one of the following values:

## -STATUS_DEVICE_NOT_READY

The keyboard interrupt is not initialized.

## -STATUS_INVALID_PARAMETER

<b>Parameters.DeviceIoControl.InputBufferLength</b> is less than the size, in bytes, of a KEYBOARD_TYPEMATIC_PARAMETERS structure, or the specified typematic settings are invalid.

## -STATUS_IO_TIMEOUT

The request timed out.

## -STATUS_SUCCESS

The request completed successfully.

## -see-also

<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_set_indicators">IOCTL_KEYBOARD_SET_INDICATORS</a>



<a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_typematic_parameters">KEYBOARD_TYPEMATIC_PARAMETERS</a>