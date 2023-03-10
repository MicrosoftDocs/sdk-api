---
UID: NS:ntddmou._MOUSE_INPUT_DATA
title: MOUSE_INPUT_DATA (ntddmou.h)
description: MOUSE_INPUT_DATA contains one packet of mouse input data.
helpviewer_keywords: ["*PMOUSE_INPUT_DATA","MOUSE_INPUT_DATA","MOUSE_INPUT_DATA structure [Human Input Devices]","PMOUSE_INPUT_DATA","PMOUSE_INPUT_DATA structure pointer [Human Input Devices]","hid.mouse_input_data","mref_7f184199-ae93-458c-8e4b-25fcacc57263.xml","ntddmou/MOUSE_INPUT_DATA","ntddmou/PMOUSE_INPUT_DATA"]
old-location: hid\mouse_input_data.htm
tech.root: hid
ms.assetid: 363699d5-e91c-43ea-bae3-8ed997487e31
ms.date: 12/05/2018
ms.keywords: '*PMOUSE_INPUT_DATA, MOUSE_INPUT_DATA, MOUSE_INPUT_DATA structure [Human Input Devices], PMOUSE_INPUT_DATA, PMOUSE_INPUT_DATA structure pointer [Human Input Devices], hid.mouse_input_data, mref_7f184199-ae93-458c-8e4b-25fcacc57263.xml, ntddmou/MOUSE_INPUT_DATA, ntddmou/PMOUSE_INPUT_DATA'
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
req.typenames: MOUSE_INPUT_DATA, *PMOUSE_INPUT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MOUSE_INPUT_DATA
 - ntddmou/_MOUSE_INPUT_DATA
 - PMOUSE_INPUT_DATA
 - ntddmou/PMOUSE_INPUT_DATA
 - MOUSE_INPUT_DATA
 - ntddmou/MOUSE_INPUT_DATA
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
 - MOUSE_INPUT_DATA
---

# MOUSE_INPUT_DATA structure


## -description

MOUSE_INPUT_DATA contains one packet of mouse input data.

## -struct-fields

### -field UnitId

Specifies the unit number of the mouse device. A mouse <a href="/windows-hardware/drivers/kernel/nt-device-names">device name</a> has the format \Device\PointerPort<i>N</i>, where the suffix <i>N </i> is the unit number of the device. For example, a device, whose name is \Device\PointerPort0, has a unit number of zero, and a device, whose name is \Device\PointerPort1, has a unit number of one.

### -field Flags

Specifies a bitwise OR of one or more of the following mouse indicator flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
MOUSE_MOVE_RELATIVE

</td>
<td>
The <b>LastX</b> and <b>LastY</b> are set relative to the previous location.

</td>
</tr>
<tr>
<td>
MOUSE_MOVE_ABSOLUTE

</td>
<td>
The <b>LastX</b> and <b>LastY</b> values are set to absolute values.

</td>
</tr>
<tr>
<td>
MOUSE_VIRTUAL_DESKTOP

</td>
<td>
The mouse coordinates are mapped to the virtual desktop.

</td>
</tr>
<tr>
<td>
MOUSE_ATTRIBUTES_CHANGED

</td>
<td>
The mouse attributes have changed. The other data in the structure is not used.

</td>
</tr>
<tr>
<td>
MOUSE_MOVE_NOCOALESCE

</td>
<td>
(Windows Vista and later) WM_MOUSEMOVE notification messages will not be coalesced. By default, these messages are coalesced.

For more information about WM_MOUSEMOVE notification messages, see the Microsoft Software Development Kit (SDK) documentation

</td>
</tr>
</table>

### -field Buttons

Specifies both <b>ButtonFlags</b> and <b>ButtonData</b> values. Mouclass uses <b>Buttons</b> in its interrupt service routine to do a fast single memory access to <b>ButtonFlags</b> and <b>ButtonData</b>.

### -field ButtonFlags

Specifies the transition state of the mouse buttons.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
MOUSE_LEFT_BUTTON_DOWN

</td>
<td>
The left mouse button changed to down.

</td>
</tr>
<tr>
<td>
MOUSE_LEFT_BUTTON_UP

</td>
<td>
The left mouse button changed to up.

</td>
</tr>
<tr>
<td>
MOUSE_RIGHT_BUTTON_DOWN

</td>
<td>
The right mouse button changed to down.

</td>
</tr>
<tr>
<td>
MOUSE_RIGHT_BUTTON_UP

</td>
<td>
The right mouse button changed to up.

</td>
</tr>
<tr>
<td>
MOUSE_MIDDLE_BUTTON_DOWN

</td>
<td>
The middle mouse button changed to down.

</td>
</tr>
<tr>
<td>
MOUSE_MIDDLE_BUTTON_UP

</td>
<td>
The middle mouse button changed to up.

</td>
</tr>
<tr>
<td>
MOUSE_BUTTON_4_DOWN

</td>
<td>
The fourth mouse button changed to down.

</td>
</tr>
<tr>
<td>
MOUSE_BUTTON_4_UP

</td>
<td>
The fourth mouse button changed to up.

</td>
</tr>
<tr>
<td>
MOUSE_BUTTON_5_DOWN

</td>
<td>
The fifth mouse button changed to down.

</td>
</tr>
<tr>
<td>
MOUSE_BUTTON_5_UP

</td>
<td>
The fifth mouse button changed to up.

</td>
</tr>
<tr>
<td>
MOUSE_WHEEL

</td>
<td>
Mouse wheel data is present.

</td>
</tr>
<tr>
<td>
MOUSE_HWHEEL

</td>
<td>
Mouse horizontal wheel data is present.

</td>
</tr>
</table>

### -field ButtonData

Specifies mouse wheel data, if MOUSE_WHEEL is set in ButtonFlags.

### -field RawButtons

Specifies the raw state of the mouse buttons. The Win32 subsystem does not use this member.

### -field LastX

Specifies the signed relative or absolute motion in the x direction.

### -field LastY

Specifies the signed relative or absolute motion in the y direction.

### -field ExtraInformation

Specifies device-specific information.

## -remarks

In response to <a href="/previous-versions/ff542215(v=vs.85)">IRP_MJ_READ (Mouclass)</a> requests, Mouclass transfers zero or more <b>MOUSE_INPUT_DATA</b> structures from its internal data queue to the Microsoft Win32 subsystem buffer.

## -see-also

<a href="/previous-versions/ff542215(v=vs.85)">IRP_MJ_READ (Mouclass)</a>



<a href="/previous-versions/ff542394(v=vs.85)">MouseClassServiceCallback</a>