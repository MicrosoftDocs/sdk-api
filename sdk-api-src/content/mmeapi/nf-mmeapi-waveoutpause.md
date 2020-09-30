---
UID: NF:mmeapi.waveOutPause
title: waveOutPause function (mmeapi.h)
description: The waveOutPause function pauses playback on the given waveform-audio output device. The current position is saved. Use the waveOutRestart function to resume playback from the current position.
helpviewer_keywords: ["_win32_waveOutPause","mmeapi/waveOutPause","multimedia.waveoutpause","waveOutPause","waveOutPause function [Windows Multimedia]"]
old-location: multimedia\waveoutpause.htm
tech.root: Multimedia
ms.assetid: a54eb1f4-fa80-4995-a70f-1aa480f46e86
ms.date: 12/05/2018
ms.keywords: _win32_waveOutPause, mmeapi/waveOutPause, multimedia.waveoutpause, waveOutPause, waveOutPause function [Windows Multimedia]
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
 - waveOutPause
 - mmeapi/waveOutPause
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
 - waveOutPause
---

# waveOutPause function


## -description

The <b>waveOutPause</b> function pauses playback on the given waveform-audio output device. The current position is saved. Use the <a href="/previous-versions/dd743871(v=vs.85)">waveOutRestart</a> function to resume playback from the current position.

## -parameters

### -param hwo

Handle to the waveform-audio output device.

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
Specified device is synchronous and does not support pausing.

</td>
</tr>
</table>

## -remarks

Calling this function when the output is already paused has no effect, and the function returns zero.

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>