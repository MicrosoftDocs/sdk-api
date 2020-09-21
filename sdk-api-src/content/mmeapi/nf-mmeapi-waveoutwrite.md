---
UID: NF:mmeapi.waveOutWrite
title: waveOutWrite function (mmeapi.h)
description: The waveOutWrite function sends a data block to the given waveform-audio output device.
helpviewer_keywords: ["_win32_waveOutWrite","mmeapi/waveOutWrite","multimedia.waveoutwrite","waveOutWrite","waveOutWrite function [Windows Multimedia]"]
old-location: multimedia\waveoutwrite.htm
tech.root: Multimedia
ms.assetid: d687b136-8ce3-43fc-b459-b12a3fe862c8
ms.date: 12/05/2018
ms.keywords: _win32_waveOutWrite, mmeapi/waveOutWrite, multimedia.waveoutwrite, waveOutWrite, waveOutWrite function [Windows Multimedia]
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
 - waveOutWrite
 - mmeapi/waveOutWrite
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
 - waveOutWrite
---

# waveOutWrite function


## -description

The <b>waveOutWrite</b> function sends a data block to the given waveform-audio output device.

## -parameters

### -param hwo

Handle to the waveform-audio output device.

### -param pwh

Pointer to a <a href="/previous-versions/dd743837(v=vs.85)">WAVEHDR</a> structure containing information about the data block.

### -param cbwh

Size, in bytes, of the <b>WAVEHDR</b> structure.

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
<dt><b>WAVERR_UNPREPARED</b></dt>
</dl>
</td>
<td width="60%">
The data block pointed to by the <i>pwh</i> parameter hasn't been prepared.

</td>
</tr>
</table>

## -remarks

When the buffer is finished, the WHDR_DONE bit is set in the <b>dwFlags</b> member of the <b>WAVEHDR</b> structure.

The buffer must be prepared with the <b>waveOutPrepareHeader</b> function before it is passed to <b>waveOutWrite</b>. Unless the device is paused by calling the <b>waveOutPause</b> function, playback begins when the first data block is sent to the device.

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>