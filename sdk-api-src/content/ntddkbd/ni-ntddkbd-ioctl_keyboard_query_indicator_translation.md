---
UID: NI:ntddkbd.IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION
title: IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION (ntddkbd.h)
description: The IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION request returns information about the mapping between scan codes and keyboard indicators.
helpviewer_keywords: ["IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION","IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION control","IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION control code [Human Input Devices]","hid.ioctl_keyboard_query_indicator_translation2","i8042ref_e1b419fa-c16e-4fe4-9534-5ae074cbb238.xml","ntddkbd/IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION"]
old-location: hid\ioctl_keyboard_query_indicator_translation2.htm
tech.root: hid
ms.assetid: b8d139e1-9465-41bd-b5e3-bc8f79f85d96
ms.date: 12/05/2018
ms.keywords: IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION, IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION control, IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION control code [Human Input Devices], hid.ioctl_keyboard_query_indicator_translation2, i8042ref_e1b419fa-c16e-4fe4-9534-5ae074cbb238.xml, ntddkbd/IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION
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
 - IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION
 - ntddkbd/IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION
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
 - IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION
---

# IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION IOCTL


## -description

The IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION request returns information about the mapping between scan codes and keyboard indicators.

## -ioctlparameters

### -input-buffer

<b>Parameters.DeviceIoControl.OutputBufferLength</b> is set to a value greater than or equal to the size, in bytes, of a device-specific <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_indicator_translation">KEYBOARD_INDICATOR_TRANSLATION</a> structure. This structure includes a variable-sized array of INDICATOR_LIST members that is device-specific.

### -input-buffer-length

 The size of a <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_indicator_translation">KEYBOARD_INDICATOR_TRANSLATION</a> structure.

### -output-buffer

<b>AssociatedIrp.SystemBuffer</b> points to a client-allocated buffer that I8042prt uses to output a <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_indicator_translation">KEYBOARD_INDICATOR_TRANSLATION</a> structure. This structure includes a variable-sized array of INDICATOR_LIST members that is device-specific.

### -output-buffer-length

 The size of a <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_indicator_translation">KEYBOARD_INDICATOR_TRANSLATION</a> structure.

### -in-out-buffer


### -inout-buffer-length


### -status-block

If the request is successful, the <b>Information</b> member is set to the size, in bytes, of the device-specific KEYBOARD_INDICATOR_TRANSLATION structure. Otherwise, <b>Information</b> is set to zero.

The <b>Status</b> member is set to one of the following values:

## -STATUS_BUFFER_TOO_SMALL

<b>Parameters.DeviceIoControl.OutputBufferLength</b> is less than the size, in bytes, of the device-specific KEYBOARD_INDICATOR_TRANSLATION structure.

## -STATUS_SUCCESS

The request completed successfully.

## -see-also

<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_attributes">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_indicators">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_typematic">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_indicator_translation">KEYBOARD_INDICATOR_TRANSLATION</a>