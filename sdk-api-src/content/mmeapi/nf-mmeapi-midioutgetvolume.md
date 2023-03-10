---
UID: NF:mmeapi.midiOutGetVolume
title: midiOutGetVolume function (mmeapi.h)
description: The midiOutGetVolume function retrieves the current volume setting of a MIDI output device.
helpviewer_keywords: ["_win32_midiOutGetVolume","midiOutGetVolume","midiOutGetVolume function [Windows Multimedia]","mmeapi/midiOutGetVolume","multimedia.midioutgetvolume"]
old-location: multimedia\midioutgetvolume.htm
tech.root: Multimedia
ms.assetid: d0e2d5e8-9fb9-4f4c-9b17-6d67b3f82ef7
ms.date: 12/05/2018
ms.keywords: _win32_midiOutGetVolume, midiOutGetVolume, midiOutGetVolume function [Windows Multimedia], mmeapi/midiOutGetVolume, multimedia.midioutgetvolume
req.header: mmeapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - midiOutGetVolume
 - mmeapi/midiOutGetVolume
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
 - midiOutGetVolume
---

# midiOutGetVolume function


## -description

The <b>midiOutGetVolume</b> function retrieves the current volume setting of a MIDI output device.

## -parameters

### -param hmo

Handle to an open MIDI output device. This parameter can also contain the handle of a MIDI stream, as long as it is cast to <b>HMIDIOUT</b>. This parameter can also be a device identifier.

### -param pdwVolume

Pointer to the location to contain the current volume setting. The low-order word of this location contains the left-channel volume setting, and the high-order word contains the right-channel setting. A value of 0xFFFF represents full volume, and a value of 0x0000 is silence.

If a device does not support both left and right volume control, the low-order word of the specified location contains the mono volume level.

Any value set by using the <a href="/previous-versions/dd798480(v=vs.85)">midiOutSetVolume</a> function is returned, regardless of whether the device supports that value.

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
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified device handle is invalid.

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
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
The system is unable to allocate or lock memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The function is not supported.

</td>
</tr>
</table>

## -remarks

If a device identifier is used, then the result of the <b>midiOutGetVolume</b> call and the information returned in <i>lpdwVolume</i> applies to all instances of the device. If a device handle is used, then the result and information returned applies only to the instance of the device referenced by the device handle.

Not all devices support volume control. You can determine whether a device supports volume control by querying the device by using the <a href="/previous-versions/dd798469(v=vs.85)">midiOutGetDevCaps</a> function and specifying the MIDICAPS_VOLUME flag.

You can also determine whether the device supports volume control on both the left and right channels by querying the device by using the <a href="/previous-versions/dd798469(v=vs.85)">midiOutGetDevCaps</a> function and specifying the MIDICAPS_LRVOLUME flag.

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>