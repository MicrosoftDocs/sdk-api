---
UID: NS:ntddmou._MOUSE_ATTRIBUTES
title: MOUSE_ATTRIBUTES (ntddmou.h)
description: MOUSE_ATTRIBUTES specifies the attributes of a mouse device.
helpviewer_keywords: ["*PMOUSE_ATTRIBUTES","MOUSE_ATTRIBUTES","MOUSE_ATTRIBUTES structure [Human Input Devices]","PMOUSE_ATTRIBUTES","PMOUSE_ATTRIBUTES structure pointer [Human Input Devices]","hid.mouse_attributes","mref_22017a48-dbf7-430b-ad42-908dc16fbaff.xml","ntddmou/MOUSE_ATTRIBUTES","ntddmou/PMOUSE_ATTRIBUTES"]
old-location: hid\mouse_attributes.htm
tech.root: hid
ms.assetid: e1054d4c-e149-4ebd-9336-2a1060e1e53d
ms.date: 12/05/2018
ms.keywords: '*PMOUSE_ATTRIBUTES, MOUSE_ATTRIBUTES, MOUSE_ATTRIBUTES structure [Human Input Devices], PMOUSE_ATTRIBUTES, PMOUSE_ATTRIBUTES structure pointer [Human Input Devices], hid.mouse_attributes, mref_22017a48-dbf7-430b-ad42-908dc16fbaff.xml, ntddmou/MOUSE_ATTRIBUTES, ntddmou/PMOUSE_ATTRIBUTES'
req.header: ntddmou.h
req.include-header: Ntddmou.h
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
req.typenames: MOUSE_ATTRIBUTES, *PMOUSE_ATTRIBUTES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MOUSE_ATTRIBUTES
 - ntddmou/_MOUSE_ATTRIBUTES
 - PMOUSE_ATTRIBUTES
 - ntddmou/PMOUSE_ATTRIBUTES
 - MOUSE_ATTRIBUTES
 - ntddmou/MOUSE_ATTRIBUTES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddmou.h
api_name:
 - MOUSE_ATTRIBUTES
---

# MOUSE_ATTRIBUTES structure


## -description

MOUSE_ATTRIBUTES specifies the attributes of a mouse device.

## -struct-fields

### -field MouseIdentifier

Specifies one of the following types of mouse devices.

<table>
<tr>
<th>Mouse type</th>
<th>Meaning</th>
</tr>
<tr>
<td>
BALLPOINT_I8042_HARDWARE

</td>
<td>
i8042 port ballpoint mouse

</td>
</tr>
<tr>
<td>
BALLPOINT_SERIAL_HARDWARE

</td>
<td>
Serial port ballpoint mouse

</td>
</tr>
<tr>
<td>
MOUSE_HID_HARDWARE

</td>
<td>
HIDClass mouse

</td>
</tr>
<tr>
<td>
MOUSE_I8042_HARDWARE

</td>
<td>
i8042 port mouse

</td>
</tr>
<tr>
<td>
MOUSE_INPORT_HARDWARE

</td>
<td>
Inport (bus) mouse

</td>
</tr>
<tr>
<td>
MOUSE_SERIAL_HARDWARE

</td>
<td>
Serial port mouse

</td>
</tr>
<tr>
<td>
WHEELMOUSE_HID_HARDWARE

</td>
<td>
HIDClass wheel mouse

</td>
</tr>
<tr>
<td>
WHEELMOUSE_I8042_HARDWARE

</td>
<td>
i8042 port wheel mouse

</td>
</tr>
<tr>
<td>
WHEELMOUSE_SERIAL_HARDWARE

</td>
<td>
Serial port wheel mouse

</td>
</tr>
</table>

### -field NumberOfButtons

Specifies the number of buttons supported by a mouse. A mouse can have from two to five buttons. The default value is MOUSE_NUMBER_OF_BUTTONS.

### -field SampleRate

Specifies the rate, in reports per second, at which input from a PS/2 mouse is sampled. The default value is MOUSE_SAMPLE_RATE. This value is not used for USB devices.

### -field InputDataQueueLength

Specifies the size, in bytes, of the input data queue used by the port driver for a mouse device.

## -remarks

This structure is used with an <a href="/windows/desktop/api/ntddmou/ni-ntddmou-ioctl_mouse_query_attributes">IOCTL_MOUSE_QUERY_ATTRIBUTES</a> request to obtain the attributes of a mouse.

## -see-also

<a href="/windows/desktop/api/ntddmou/ni-ntddmou-ioctl_mouse_query_attributes">IOCTL_MOUSE_QUERY_ATTRIBUTES</a>