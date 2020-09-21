---
UID: NF:mmeapi.midiOutSetVolume
title: midiOutSetVolume function (mmeapi.h)
description: The midiOutSetVolume function sets the volume of a MIDI output device.
helpviewer_keywords: ["_win32_midiOutSetVolume","midiOutSetVolume","midiOutSetVolume function [Windows Multimedia]","mmeapi/midiOutSetVolume","multimedia.midioutsetvolume"]
old-location: multimedia\midioutsetvolume.htm
tech.root: Multimedia
ms.assetid: a24ff9fa-06d1-4124-ab66-1cdcabacbc4c
ms.date: 12/05/2018
ms.keywords: _win32_midiOutSetVolume, midiOutSetVolume, midiOutSetVolume function [Windows Multimedia], mmeapi/midiOutSetVolume, multimedia.midioutsetvolume
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
 - midiOutSetVolume
 - mmeapi/midiOutSetVolume
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
 - midiOutSetVolume
---

# midiOutSetVolume function


## -description

The <b>midiOutSetVolume</b> function sets the volume of a MIDI output device.

## -parameters

### -param hmo

Handle to an open MIDI output device. This parameter can also contain the handle of a MIDI stream, as long as it is cast to <b>HMIDIOUT</b>. This parameter can also be a device identifier.

### -param dwVolume

New volume setting. The low-order word contains the left-channel volume setting, and the high-order word contains the right-channel setting. A value of 0xFFFF represents full volume, and a value of 0x0000 is silence.

If a device does not support both left and right volume control, the low-order word of <i>dwVolume</i> specifies the mono volume level, and the high-order word is ignored.

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

If a device identifier is used, then the result of the <b>midiOutSetVolume</b> call applies to all instances of the device. If a device handle is used, then the result applies only to the instance of the device referenced by the device handle.

Not all devices support volume changes. You can determine whether a device supports it by querying the device using the <a href="/previous-versions/dd798469(v=vs.85)">midiOutGetDevCaps</a> function and the MIDICAPS_VOLUME flag.

You can also determine whether the device supports volume control on both the left and right channels by querying the device using the <a href="/previous-versions/dd798469(v=vs.85)">midiOutGetDevCaps</a> function and the MIDICAPS_LRVOLUME flag.

Devices that do not support a full 16 bits of volume-level control use the high-order bits of the requested volume setting. For example, a device that supports 4 bits of volume control produces the same volume setting for the following volume-level values: 0x4000, 0x43be, and 0x4fff. The <a href="/previous-versions/dd798473(v=vs.85)">midiOutGetVolume</a> function returns the full 16-bit value, as set by <b>midiOutSetVolume</b>, irrespective of the device's capabilities.

Volume settings are interpreted logarithmically. This means that the perceived increase in volume is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>