---
UID: NI:ntddkbd.IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES
title: IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES (ntddkbd.h)
description: The IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES request returns information about the extended keyboard attributes.
helpviewer_keywords: ["IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES","IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES control","IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES control code [Human Input Devices]","hid.IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES2","ntddkbd/IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES"]
tech.root: hid
ms.assetid: 5fb8a728-7166-400d-b41d-914a4847095a
ms.date: 07/17/2020
ms.keywords: IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES, IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES control, IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES control code [Human Input Devices], hid.IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES2, ntddkbd/IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES
f1_keywords:
- ntddkbd/IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES
dev_langs:
- c++
req.header: ntddkbd.h
req.include-header: Ntddkbd.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
- IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES IOCTL

## -description

The IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES request returns information about the extended keyboard attributes.

## -ioctlparameters

### -input-buffer

**Parameters.DeviceIoControl.OutputBufferLength** is set to a value greater than or equal to the size, in bytes, of a [KEYBOARD_EXTENDED_ATTRIBUTES](ns-ntddkbd-keyboard_extended_attributes.md) structure.

### -input-buffer-length

The size of a [KEYBOARD_EXTENDED_ATTRIBUTES](ns-ntddkbd-keyboard_extended_attributes.md) structure.

### -output-buffer

**AssociatedIrp.SystemBuffer** points to a client-allocated buffer that I8042prt uses to output a [KEYBOARD_EXTENDED_ATTRIBUTES](ns-ntddkbd-keyboard_extended_attributes.md) structure.

### -output-buffer-length

The size of a [KEYBOARD_EXTENDED_ATTRIBUTES](ns-ntddkbd-keyboard_extended_attributes.md) structure.

### -in-out-buffer

### -inout-buffer-length

### -status-block

If the request is successful, the **Information** member is set to the size, in bytes, of a KEYBOARD_EXTENDED_ATTRIBUTES structure. Otherwise the **Information** member is set to zero.

The **Status** member is set to one of the following values:

#### -STATUS_BUFFER_TOO_SMALL

**Parameters.DeviceIoControl.OutputBufferLength** is less than the size, in bytes, of a KEYBOARD_EXTENDED_ATTRIBUTES structure.

#### -STATUS_SUCCESS

The request completed successfully.

## -see-also

[KEYBOARD_EXTENDED_ATTRIBUTES structure](ns-ntddkbd-keyboard_extended_attributes.md)

[IOCTL_KEYBOARD_QUERY_ATTRIBUTES](ni-ntddkbd-ioctl_keyboard_query_attributes.md)

[IOCTL_KEYBOARD_QUERY_INDICATORS](ni-ntddkbd-ioctl_keyboard_query_indicators.md)

[IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION](ni-ntddkbd-ioctl_keyboard_query_indicator_translation.md)

[IOCTL_KEYBOARD_QUERY_TYPEMATIC](ni-ntddkbd-ioctl_keyboard_query_typematic.md)
