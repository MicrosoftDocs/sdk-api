---
UID: NF:mmeapi.midiInGetDevCapsW
title: midiInGetDevCapsW function (mmeapi.h)
description: The midiInGetDevCapsW (Unicode) function (mmeapi.h) determines the capabilities of a specified MIDI input device.
helpviewer_keywords: ["_win32_midiInGetDevCaps", "midiInGetDevCaps", "midiInGetDevCaps function [Windows Multimedia]", "midiInGetDevCapsW", "mmeapi/midiInGetDevCaps", "mmeapi/midiInGetDevCapsW", "multimedia.midiingetdevcaps"]
old-location: multimedia\midiingetdevcaps.htm
tech.root: Multimedia
ms.assetid: c3104427-69a9-434f-9f4e-780c96940c21
ms.date: 08/05/2022
ms.keywords: _win32_midiInGetDevCaps, midiInGetDevCaps, midiInGetDevCaps function [Windows Multimedia], midiInGetDevCapsA, midiInGetDevCapsW, mmeapi/midiInGetDevCaps, mmeapi/midiInGetDevCapsA, mmeapi/midiInGetDevCapsW, multimedia.midiingetdevcaps
req.header: mmeapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: midiInGetDevCapsW (Unicode) and midiInGetDevCapsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - midiInGetDevCapsW
 - mmeapi/midiInGetDevCapsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-mme-l1-1-0.dll
 - winmmbase.dll
api_name:
 - midiInGetDevCaps
 - midiInGetDevCapsA
 - midiInGetDevCapsW
---

# midiInGetDevCapsW function


## -description

The <b>midiInGetDevCaps</b> function determines the capabilities of a specified MIDI input device.

## -parameters

### -param uDeviceID

Identifier of the MIDI input device. The device identifier varies from zero to one less than the number of devices present. This parameter can also be a properly cast device handle.

### -param pmic

Pointer to a <a href="/previous-versions/dd798451(v=vs.85)">MIDIINCAPS</a> structure that is filled with information about the capabilities of the device.

### -param cbmic

Size, in bytes, of the <a href="/previous-versions/dd798451(v=vs.85)">MIDIINCAPS</a> structure. Only <i>cbMidiInCaps</i> bytes (or less) of information is copied to the location pointed to by <i>lpMidiInCaps</i>. If <i>cbMidiInCaps</i> is zero, nothing is copied, and the function returns MMSYSERR_NOERROR.

## -returns

Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_BADDEVICEID</b></dt>
</dl>
</td>
<td width="60%">
The specified device identifier is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
The specified pointer or structure is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NODRIVER</b></dt>
</dl>
</td>
<td width="60%">
The driver is not installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
The system is unable to allocate or lock memory.

</td>
</tr>
</table>

## -remarks

To determine the number of MIDI input devices present on the system, use the <a href="/previous-versions/dd798456(v=vs.85)">midiInGetNumDevs</a> function.





> [!NOTE]
> The mmeapi.h header defines midiInGetDevCaps as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>
