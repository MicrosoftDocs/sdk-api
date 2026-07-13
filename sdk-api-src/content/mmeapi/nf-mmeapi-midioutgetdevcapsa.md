---
UID: NF:mmeapi.midiOutGetDevCapsA
title: midiOutGetDevCapsA function (mmeapi.h)
description: The midiOutGetDevCaps function queries a specified MIDI output device to determine its capabilities. (midiOutGetDevCapsA)
helpviewer_keywords: ["midiOutGetDevCapsA", "mmeapi/midiOutGetDevCapsA"]
old-location: multimedia\midioutgetdevcaps.htm
tech.root: Multimedia
ms.assetid: 8777a903-fd47-4f3f-b534-1e72a5951846
ms.date: 12/05/2018
ms.keywords: _win32_midiOutGetDevCaps, midiOutGetDevCaps, midiOutGetDevCaps function [Windows Multimedia], midiOutGetDevCapsA, midiOutGetDevCapsW, mmeapi/midiOutGetDevCaps, mmeapi/midiOutGetDevCapsA, mmeapi/midiOutGetDevCapsW, multimedia.midioutgetdevcaps
req.header: mmeapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: midiOutGetDevCapsW (Unicode) and midiOutGetDevCapsA (ANSI)
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
 - midiOutGetDevCapsA
 - mmeapi/midiOutGetDevCapsA
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
 - midiOutGetDevCaps
 - midiOutGetDevCapsA
 - midiOutGetDevCapsW
---

# midiOutGetDevCapsA function


## -description

The <b>midiOutGetDevCaps</b> function queries a specified MIDI output device to determine its capabilities.

## -parameters

### -param uDeviceID

Identifier of the MIDI output device. The device identifier specified by this parameter varies from zero to one less than the number of devices present. The MIDI_MAPPER constant is also a valid device identifier.

This parameter can also be a properly cast device handle.

### -param pmoc

Pointer to a <a href="/previous-versions/dd798467(v=vs.85)">MIDIOUTCAPS</a> structure. This structure is filled with information about the capabilities of the device.

### -param cbmoc

Size, in bytes, of the <a href="/previous-versions/dd798467(v=vs.85)">MIDIOUTCAPS</a> structure. Only <i>cbMidiOutCaps</i> bytes (or less) of information is copied to the location pointed to by <i>lpMidiOutCaps</i>. If <i>cbMidiOutCaps</i> is zero, nothing is copied, and the function returns MMSYSERR_NOERROR.

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
The system is unable to load mapper string description.

</td>
</tr>
</table>

## -remarks

To determine the number of MIDI output devices present in the system, use the <a href="/previous-versions/dd798472(v=vs.85)">midiOutGetNumDevs</a> function.





> [!NOTE]
> The mmeapi.h header defines midiOutGetDevCaps as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>
