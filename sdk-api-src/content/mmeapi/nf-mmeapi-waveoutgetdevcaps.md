---
UID: NF:mmeapi.waveOutGetDevCaps
title: waveOutGetDevCaps function (mmeapi.h)
description: The waveOutGetDevCaps function retrieves the capabilities of a given waveform-audio output device.
helpviewer_keywords: ["_win32_waveOutGetDevCaps","mmeapi/waveOutGetDevCaps","multimedia.waveoutgetdevcaps","waveOutGetDevCaps","waveOutGetDevCaps function [Windows Multimedia]"]
old-location: multimedia\waveoutgetdevcaps.htm
tech.root: Multimedia
ms.assetid: 294daf81-d52a-44b4-b22a-d75ad6e05fee
ms.date: 12/05/2018
ms.keywords: _win32_waveOutGetDevCaps, mmeapi/waveOutGetDevCaps, multimedia.waveoutgetdevcaps, waveOutGetDevCaps, waveOutGetDevCaps function [Windows Multimedia]
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
 - waveOutGetDevCaps
 - mmeapi/waveOutGetDevCaps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
api_name:
 - waveOutGetDevCaps
---

# waveOutGetDevCaps function


## -description

The <b>waveOutGetDevCaps</b> function retrieves the capabilities of a given waveform-audio output device.

## -parameters

### -param uDeviceID

Identifier of the waveform-audio output device. It can be either a device identifier or a handle of an open waveform-audio output device.

### -param pwoc

Pointer to a <a href="/previous-versions/dd743855(v=vs.85)">WAVEOUTCAPS</a> structure to be filled with information about the capabilities of the device.

### -param cbwoc

Size, in bytes, of the <b>WAVEOUTCAPS</b> structure.

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
Specified device identifier is out of range.

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
</table>

## -remarks

Use the <b>waveOutGetNumDevs</b> function to determine the number of waveform-audio output devices present in the system. If the value specified by the <i>uDeviceID</i> parameter is a device identifier, it can vary from zero to one less than the number of devices present. The WAVE_MAPPER constant can also be used as a device identifier. Only <i>cbwoc</i> bytes (or less) of information is copied to the location pointed to by <i>pwoc</i>. If <i>cbwoc</i> is zero, nothing is copied and the function returns zero.

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>