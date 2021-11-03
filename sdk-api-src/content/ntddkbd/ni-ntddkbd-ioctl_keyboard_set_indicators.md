---
UID: NI:ntddkbd.IOCTL_KEYBOARD_SET_INDICATORS
title: IOCTL_KEYBOARD_SET_INDICATORS (ntddkbd.h)
description: The IOCTL_KEYBOARD_SET_INDICATORS request sets the keyboard indicators.
helpviewer_keywords: ["IOCTL_KEYBOARD_SET_INDICATORS","IOCTL_KEYBOARD_SET_INDICATORS control","IOCTL_KEYBOARD_SET_INDICATORS control code [Human Input Devices]","hid.ioctl_keyboard_set_indicators2","i8042ref_45e33d11-eb35-4f90-b7c8-52f75afb60ef.xml","ntddkbd/IOCTL_KEYBOARD_SET_INDICATORS"]
old-location: hid\ioctl_keyboard_set_indicators2.htm
tech.root: hid
ms.assetid: 34b25d9d-daa5-48c6-8941-f3795ef1802b
ms.date: 12/05/2018
ms.keywords: IOCTL_KEYBOARD_SET_INDICATORS, IOCTL_KEYBOARD_SET_INDICATORS control, IOCTL_KEYBOARD_SET_INDICATORS control code [Human Input Devices], hid.ioctl_keyboard_set_indicators2, i8042ref_45e33d11-eb35-4f90-b7c8-52f75afb60ef.xml, ntddkbd/IOCTL_KEYBOARD_SET_INDICATORS
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
 - IOCTL_KEYBOARD_SET_INDICATORS
 - ntddkbd/IOCTL_KEYBOARD_SET_INDICATORS
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
 - IOCTL_KEYBOARD_SET_INDICATORS
---

# IOCTL_KEYBOARD_SET_INDICATORS IOCTL


## -description

The IOCTL_KEYBOARD_SET_INDICATORS request sets the keyboard indicators.

## -ioctlparameters

### -input-buffer

<b>AssociatedIrp.SystemBuffer</b> points to a client-allocated buffer that inputs a <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_indicator_parameters">KEYBOARD_INDICATOR_PARAMETERS</a> structure. The client sets the indicator parameters in this structure.

<b>Parameters.DeviceIoControl.InputBufferLength</b> is set to a value greater than or equal to the size, in bytes, of a <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_indicator_parameters">KEYBOARD_INDICATOR_PARAMETERS</a> structure.

### -input-buffer-length

The size of a <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_indicator_parameters">KEYBOARD_INDICATOR_PARAMETERS</a> structure.

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

<b>Parameters.DeviceIoControl.InputBufferLength</b> is less than the size, in bytes, of a KEYBOARD_INDICATOR_PARAMETERS structure, or the specified indicator parameters are invalid.

## -STATUS_IO_TIMEOUT

The request timed out.

## -STATUS_SUCCESS

The request completed successfully.

## -see-also

<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_set_typematic">IOCTL_KEYBOARD_SET_TYPEMATIC</a>



<a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_indicator_parameters">KEYBOARD_INDICATOR_PARAMETERS</a>