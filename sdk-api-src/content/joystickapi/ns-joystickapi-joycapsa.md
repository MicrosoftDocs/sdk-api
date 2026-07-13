---
UID: NS:joystickapi.tagJOYCAPSA
title: JOYCAPSA (joystickapi.h)
description: The JOYCAPS structure contains information about the joystick capabilities. (JOYCAPSA)
helpviewer_keywords: ["*LPJOYCAPSA","*NPJOYCAPSA","*PJOYCAPSA","JOYCAPS","JOYCAPS structure [Windows Multimedia]","JOYCAPSA","JOYCAPSW","_win32_JOYCAPS_str","joystickapi/JOYCAPS","joystickapi/JOYCAPSA","joystickapi/JOYCAPSW","multimedia.joycaps","tagJOYCAPSA","tagJOYCAPSW"]
old-location: multimedia\joycaps.htm
tech.root: Multimedia
ms.assetid: 9b175aaf-f408-4fe8-bd7c-56f513b57c1b
ms.date: 12/05/2018
ms.keywords: '*LPJOYCAPSA, *NPJOYCAPSA, *PJOYCAPSA, JOYCAPS, JOYCAPS structure [Windows Multimedia], JOYCAPSA, JOYCAPSW, _win32_JOYCAPS_str, joystickapi/JOYCAPS, joystickapi/JOYCAPSA, joystickapi/JOYCAPSW, multimedia.joycaps, tagJOYCAPSA, tagJOYCAPSW'
req.header: joystickapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: JOYCAPSW (Unicode) and JOYCAPSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: JOYCAPSA, *PJOYCAPSA, *NPJOYCAPSA, *LPJOYCAPSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagJOYCAPSA
 - joystickapi/tagJOYCAPSA
 - PJOYCAPSA
 - joystickapi/PJOYCAPSA
 - JOYCAPSA
 - joystickapi/JOYCAPSA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - joystickapi.h
api_name:
 - JOYCAPS
 - JOYCAPSA
 - JOYCAPSW
---

# JOYCAPSA structure


## -description

The <b>JOYCAPS</b> structure contains information about the joystick capabilities.

## -struct-fields

### -field wMid

Manufacturer identifier. Manufacturer identifiers are defined in <a href="/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.

### -field wPid

Product identifier. Product identifiers are defined in <a href="/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.

### -field szPname

Null-terminated string containing the joystick product name.

### -field wXmin

Minimum X-coordinate.

### -field wXmax

Maximum X-coordinate.

### -field wYmin

Minimum Y-coordinate.

### -field wYmax

Maximum Y-coordinate.

### -field wZmin

Minimum Z-coordinate.

### -field wZmax

Maximum Z-coordinate.

### -field wNumButtons

Number of joystick buttons.

### -field wPeriodMin

Smallest polling frequency supported when captured by the <a href="/previous-versions/dd757114(v=vs.85)">joySetCapture</a> function.

### -field wPeriodMax

Largest polling frequency supported when captured by <b>joySetCapture</b>.

### -field wRmin

Minimum rudder value. The rudder is a fourth axis of movement.

### -field wRmax

Maximum rudder value. The rudder is a fourth axis of movement.

### -field wUmin

Minimum u-coordinate (fifth axis) values.

### -field wUmax

Maximum u-coordinate (fifth axis) values.

### -field wVmin

Minimum v-coordinate (sixth axis) values.

### -field wVmax

Maximum v-coordinate (sixth axis) values.

### -field wCaps

Joystick capabilities The following flags define individual capabilities that a joystick might have:

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>JOYCAPS_HASZ</td>
<td>Joystick has z-coordinate information.</td>
</tr>
<tr>
<td>JOYCAPS_HASR</td>
<td>Joystick has rudder (fourth axis) information.</td>
</tr>
<tr>
<td>JOYCAPS_HASU</td>
<td>Joystick has u-coordinate (fifth axis) information.</td>
</tr>
<tr>
<td>JOYCAPS_HASV</td>
<td>Joystick has v-coordinate (sixth axis) information.</td>
</tr>
<tr>
<td>JOYCAPS_HASPOV</td>
<td>Joystick has point-of-view information.</td>
</tr>
<tr>
<td>JOYCAPS_POV4DIR</td>
<td>Joystick point-of-view supports discrete values (centered, forward, backward, left, and right).</td>
</tr>
<tr>
<td>JOYCAPS_POVCTS</td>
<td>Joystick point-of-view supports continuous degree bearings.</td>
</tr>
</table>

### -field wMaxAxes

Maximum number of axes supported by the joystick.

### -field wNumAxes

Number of axes currently in use by the joystick.

### -field wMaxButtons

Maximum number of buttons supported by the joystick.

### -field szRegKey

Null-terminated string containing the registry key for the joystick.

### -field szOEMVxD

Null-terminated string identifying the joystick driver OEM.

## -see-also

Joysticks



Multimedia Joystick Structures



<a href="/previous-versions/dd757114(v=vs.85)">joySetCapture</a>

## -remarks

> [!NOTE]
> The joystickapi.h header defines JOYCAPS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
