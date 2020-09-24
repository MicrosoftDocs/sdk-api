---
UID: NF:mmeapi.waveOutSetVolume
title: waveOutSetVolume function (mmeapi.h)
description: The waveOutSetVolume function sets the volume level of the specified waveform-audio output device.
helpviewer_keywords: ["_win32_waveOutSetVolume","mmeapi/waveOutSetVolume","multimedia.waveoutsetvolume","waveOutSetVolume","waveOutSetVolume function [Windows Multimedia]"]
old-location: multimedia\waveoutsetvolume.htm
tech.root: Multimedia
ms.assetid: 6dcc53ae-b663-4812-8c93-a573b8dc6e57
ms.date: 12/05/2018
ms.keywords: _win32_waveOutSetVolume, mmeapi/waveOutSetVolume, multimedia.waveoutsetvolume, waveOutSetVolume, waveOutSetVolume function [Windows Multimedia]
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
 - waveOutSetVolume
 - mmeapi/waveOutSetVolume
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
 - waveOutSetVolume
---

# waveOutSetVolume function


## -description

The <b>waveOutSetVolume</b> function sets the volume level of the specified waveform-audio output device.

## -parameters

### -param hwo

Handle to an open waveform-audio output device. This parameter can also be a device identifier.

### -param dwVolume

New volume setting. The low-order word contains the left-channel volume setting, and the high-order word contains the right-channel setting. A value of 0xFFFF represents full volume, and a value of 0x0000 is silence.

If a device does not support both left and right volume control, the low-order word of <i>dwVolume</i> specifies the volume level, and the high-order word is ignored.

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
Specified device handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NODRIVER</b></dt>
</dl>
</td>
<td width="60%">
No device driver is present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate or lock memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Function is not supported.

</td>
</tr>
</table>

## -remarks

If a device identifier is used, then the result of the <b>waveOutSetVolume</b> call applies to all instances of the device. If a device handle is used, then the result applies only to the instance of the device referenced by the device handle.

Not all devices support volume changes. To determine whether the device supports volume control, use the WAVECAPS_VOLUME flag to test the <b>dwSupport</b> member of the <a href="/previous-versions/dd743855(v=vs.85)">WAVEOUTCAPS</a> structure (filled by the <a href="/previous-versions/dd743857(v=vs.85)">waveOutGetDevCaps</a> function). To determine whether the device supports volume control on both the left and right channels, use the WAVECAPS_LRVOLUME flag.

Most devices do not support the full 16 bits of volume-level control and will not use the least-significant bits of the requested volume setting. For example, if a device supports 4 bits of volume control, the values 0x4000, 0x4FFF, and 0x43BE will all be truncated to 0x4000. The <b>waveOutGetVolume</b> function returns the full 16-bit setting set with <b>waveOutSetVolume</b>.

Volume settings are interpreted logarithmically. This means the perceived increase in volume is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>