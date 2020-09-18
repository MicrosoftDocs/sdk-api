---
UID: NF:mmeapi.waveOutGetVolume
title: waveOutGetVolume function (mmeapi.h)
description: The waveOutGetVolume function retrieves the current volume level of the specified waveform-audio output device.
helpviewer_keywords: ["_win32_waveOutGetVolume","mmeapi/waveOutGetVolume","multimedia.waveoutgetvolume","waveOutGetVolume","waveOutGetVolume function [Windows Multimedia]"]
old-location: multimedia\waveoutgetvolume.htm
tech.root: Multimedia
ms.assetid: 7f1b3ae0-8890-49f7-b249-bab934095cca
ms.date: 12/05/2018
ms.keywords: _win32_waveOutGetVolume, mmeapi/waveOutGetVolume, multimedia.waveoutgetvolume, waveOutGetVolume, waveOutGetVolume function [Windows Multimedia]
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
 - waveOutGetVolume
 - mmeapi/waveOutGetVolume
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
 - waveOutGetVolume
---

# waveOutGetVolume function


## -description

The <b>waveOutGetVolume</b> function retrieves the current volume level of the specified waveform-audio output device.

## -parameters

### -param hwo

Handle to an open waveform-audio output device. This parameter can also be a device identifier.

### -param pdwVolume

Pointer to a variable to be filled with the current volume setting. The low-order word of this location contains the left-channel volume setting, and the high-order word contains the right-channel setting. A value of 0xFFFF represents full volume, and a value of 0x0000 is silence.

If a device does not support both left and right volume control, the low-order word of the specified location contains the mono volume level.

The full 16-bit setting(s) set with the <a href="/previous-versions/dd743874(v=vs.85)">waveOutSetVolume</a> function is returned, regardless of whether the device supports the full 16 bits of volume-level control.

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
Function isn't supported.

</td>
</tr>
</table>

## -remarks

If a device identifier is used, then the result of the <b>waveOutGetVolume</b> call and the information returned in <i>pdwVolume</i> applies to all instances of the device. If a device handle is used, then the result and information returned applies only to the instance of the device referenced by the device handle.

Not all devices support volume changes. To determine whether the device supports volume control, use the WAVECAPS_VOLUME flag to test the <b>dwSupport</b> member of the <b>WAVEOUTCAPS</b> structure (filled by the <b>waveOutGetDevCaps</b> function).

To determine whether the device supports left- and right-channel volume control, use the WAVECAPS_LRVOLUME flag to test the <b>dwSupport</b> member of the <b>WAVEOUTCAPS</b> structure (filled by <b>waveOutGetDevCaps</b>).

Volume settings are interpreted logarithmically. This means the perceived increase in volume is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>