---
UID: NI:ntddkbd.IOCTL_KEYBOARD_QUERY_INDICATORS
title: IOCTL_KEYBOARD_QUERY_INDICATORS (ntddkbd.h)
description: The IOCTL_KEYBOARD_QUERY_INDICATORS request returns information about the keyboard indicators.
helpviewer_keywords: ["IOCTL_KEYBOARD_QUERY_INDICATORS","IOCTL_KEYBOARD_QUERY_INDICATORS control","IOCTL_KEYBOARD_QUERY_INDICATORS control code [Human Input Devices]","hid.ioctl_keyboard_query_indicators2","i8042ref_d34933a9-dfd8-464b-9653-7b344b5007e3.xml","ntddkbd/IOCTL_KEYBOARD_QUERY_INDICATORS"]
old-location: hid\ioctl_keyboard_query_indicators2.htm
tech.root: hid
ms.assetid: ca031026-a077-4270-addd-a0a8c22f46b6
ms.date: 12/05/2018
ms.keywords: IOCTL_KEYBOARD_QUERY_INDICATORS, IOCTL_KEYBOARD_QUERY_INDICATORS control, IOCTL_KEYBOARD_QUERY_INDICATORS control code [Human Input Devices], hid.ioctl_keyboard_query_indicators2, i8042ref_d34933a9-dfd8-464b-9653-7b344b5007e3.xml, ntddkbd/IOCTL_KEYBOARD_QUERY_INDICATORS
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
 - IOCTL_KEYBOARD_QUERY_INDICATORS
 - ntddkbd/IOCTL_KEYBOARD_QUERY_INDICATORS
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
 - IOCTL_KEYBOARD_QUERY_INDICATORS
---

# IOCTL_KEYBOARD_QUERY_INDICATORS IOCTL


## -description

The IOCTL_KEYBOARD_QUERY_INDICATORS request returns information about the keyboard indicators.

## -ioctlparameters

### -input-buffer

<b>Parameters.DeviceIoControl.OutputBufferLength</b> is set to a value greater than or equal to the size, in bytes, of a <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_indicator_parameters">KEYBOARD_INDICATOR_PARAMETERS</a> structure.

### -input-buffer-length

The size of a <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_indicator_parameters">KEYBOARD_INDICATOR_PARAMETERS</a> structure.

### -output-buffer

<b>AssociatedIrp.SystemBuffer</b> points to a client-allocated buffer that I8042prt uses to output a <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_indicator_parameters">KEYBOARD_INDICATOR_PARAMETERS</a> structure.

### -output-buffer-length

The size of  a <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_indicator_parameters">KEYBOARD_INDICATOR_PARAMETERS</a> structure.

### -in-out-buffer


### -inout-buffer-length


### -status-block

If the request is successful, the <b>Information</b> member is set to the size, in bytes, of a KEYBOARD_INDICATOR_PARAMETERS structure. Otherwise, <b>Information</b> is set to zero.

The <b>Status</b> member is set to one the following values:

## -STATUS_BUFFER_TOO_SMALL

<b>Parameters.DeviceIoControl.OutputBufferLength</b> is less than the size, in bytes, of a KEYBOARD_INDICATOR_PARAMETERS structure.

## -STATUS_SUCCESS

The request completed successfully.

## -see-also

<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_attributes">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_indicator_translation">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_typematic">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_indicator_parameters">KEYBOARD_INDICATOR_PARAMETERS</a>