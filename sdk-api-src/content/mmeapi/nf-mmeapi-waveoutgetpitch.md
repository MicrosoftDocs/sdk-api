---
UID: NF:mmeapi.waveOutGetPitch
title: waveOutGetPitch function (mmeapi.h)
description: The waveOutGetPitch function retrieves the current pitch setting for the specified waveform-audio output device.
helpviewer_keywords: ["_win32_waveOutGetPitch","mmeapi/waveOutGetPitch","multimedia.waveoutgetpitch","waveOutGetPitch","waveOutGetPitch function [Windows Multimedia]"]
old-location: multimedia\waveoutgetpitch.htm
tech.root: Multimedia
ms.assetid: e4adcf3d-2d9a-4cf3-81bc-3d109c90663f
ms.date: 12/05/2018
ms.keywords: _win32_waveOutGetPitch, mmeapi/waveOutGetPitch, multimedia.waveoutgetpitch, waveOutGetPitch, waveOutGetPitch function [Windows Multimedia]
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
 - waveOutGetPitch
 - mmeapi/waveOutGetPitch
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
 - waveOutGetPitch
---

# waveOutGetPitch function


## -description

The <b>waveOutGetPitch</b> function retrieves the current pitch setting for the specified waveform-audio output device.

## -parameters

### -param hwo

Handle to the waveform-audio output device.

### -param pdwPitch

Pointer to a variable to be filled with the current pitch multiplier setting. The pitch multiplier indicates the current change in pitch from the original authored setting. The pitch multiplier must be a positive value.

The pitch multiplier is specified as a fixed-point value. The high-order word of the variable contains the signed integer part of the number, and the low-order word contains the fractional part. A value of 0x8000 in the low-order word represents one-half, and 0x4000 represents one-quarter. For example, the value 0x00010000 specifies a multiplier of 1.0 (no pitch change), and a value of 0x000F8000 specifies a multiplier of 15.5.

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

Changing the pitch does not change the playback rate, sample rate, or playback time. Not all devices support pitch changes. To determine whether the device supports pitch control, use the WAVECAPS_PITCH flag to test the <b>dwSupport</b> member of the <b>WAVEOUTCAPS</b> structure (filled by the <b>waveOutGetDevCaps</b> function).

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>