---
UID: NS:ntddkbd._KEYBOARD_INPUT_DATA
title: KEYBOARD_INPUT_DATA (ntddkbd.h)
description: KEYBOARD_INPUT_DATA contains one packet of keyboard input data.
helpviewer_keywords: ["*PKEYBOARD_INPUT_DATA","KEYBOARD_INPUT_DATA","KEYBOARD_INPUT_DATA structure [Human Input Devices]","PKEYBOARD_INPUT_DATA","PKEYBOARD_INPUT_DATA structure pointer [Human Input Devices]","hid.keyboard_input_data","kref_5fd34b1f-6ad2-4eaf-971a-8adedb3bada9.xml","ntddkbd/KEYBOARD_INPUT_DATA","ntddkbd/PKEYBOARD_INPUT_DATA"]
old-location: hid\keyboard_input_data.htm
tech.root: hid
ms.assetid: ea0b592a-51d1-4407-9c66-b069af336e54
ms.date: 12/05/2018
ms.keywords: '*PKEYBOARD_INPUT_DATA, KEYBOARD_INPUT_DATA, KEYBOARD_INPUT_DATA structure [Human Input Devices], PKEYBOARD_INPUT_DATA, PKEYBOARD_INPUT_DATA structure pointer [Human Input Devices], hid.keyboard_input_data, kref_5fd34b1f-6ad2-4eaf-971a-8adedb3bada9.xml, ntddkbd/KEYBOARD_INPUT_DATA, ntddkbd/PKEYBOARD_INPUT_DATA'
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
req.typenames: KEYBOARD_INPUT_DATA, *PKEYBOARD_INPUT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KEYBOARD_INPUT_DATA
 - ntddkbd/_KEYBOARD_INPUT_DATA
 - PKEYBOARD_INPUT_DATA
 - ntddkbd/PKEYBOARD_INPUT_DATA
 - KEYBOARD_INPUT_DATA
 - ntddkbd/KEYBOARD_INPUT_DATA
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
 - KEYBOARD_INPUT_DATA
---

# KEYBOARD_INPUT_DATA structure


## -description

KEYBOARD_INPUT_DATA contains one packet of keyboard input data.

## -struct-fields

### -field UnitId

Specifies the unit number of a keyboard device. A keyboard device name has the format \Device\KeyboardPort<i>N</i>, where the suffix <i>N </i> is the unit number of the device. For example, a device, whose name is \Device\KeyboardPort0, has a unit number of zero, and a device, whose name is \Device\KeyboardPort1, has a unit number of one.

### -field MakeCode

Specifies the scan code associated with a key press.

### -field Flags

Specifies a bitwise OR of one or more of the following flags that indicate whether a key was pressed or released, and other miscellaneous information.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
KEY_MAKE

</td>
<td>
The key was pressed.

</td>
</tr>
<tr>
<td>
KEY_BREAK

</td>
<td>
The key was released.

</td>
</tr>
<tr>
<td>
KEY_E0

</td>
<td>
Extended scan code used to indicate special keyboard functions. 

</td>
</tr>
<tr>
<td>
KEY_E1

</td>
<td>
Extended scan code used to indicate special keyboard functions. 

</td>
</tr>
</table>

### -field Reserved

Reserved for operating system use.

### -field ExtraInformation

Specifies device-specific information associated with a keyboard event.

## -remarks

In response to an <a href="/previous-versions/ff542213(v=vs.85)">IRP_MJ_READ (Kbdclass)</a> request, Kbdclass transfers zero or more <b>KEYBOARD_INPUT_DATA</b> structures from its internal data queue to the Win32 subsystem buffer.

## -see-also

<a href="/previous-versions/ff542213(v=vs.85)">IRP_MJ_READ (Kbdclass)</a>



<a href="/previous-versions/ff542324(v=vs.85)">KeyboardClassServiceCallback</a>