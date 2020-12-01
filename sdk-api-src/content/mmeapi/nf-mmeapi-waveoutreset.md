---
UID: NF:mmeapi.waveOutReset
title: waveOutReset function (mmeapi.h)
description: The waveOutReset function stops playback on the given waveform-audio output device and resets the current position to zero. All pending playback buffers are marked as done (WHDR_DONE) and returned to the application.
helpviewer_keywords: ["_win32_waveOutReset","mmeapi/waveOutReset","multimedia.waveoutreset","waveOutReset","waveOutReset function [Windows Multimedia]"]
old-location: multimedia\waveoutreset.htm
tech.root: Multimedia
ms.assetid: 8a057dcd-985b-4ec7-be5b-c1cc2a6d1e72
ms.date: 12/05/2018
ms.keywords: _win32_waveOutReset, mmeapi/waveOutReset, multimedia.waveoutreset, waveOutReset, waveOutReset function [Windows Multimedia]
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
 - waveOutReset
 - mmeapi/waveOutReset
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
 - waveOutReset
---

# waveOutReset function


## -description

The <b>waveOutReset</b> function stops playback on the given waveform-audio output device and resets the current position to zero. All pending playback buffers are marked as done (WHDR_DONE) and returned to the application.

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

After this function returns, the application can send new playback buffers to the device by calling <a href="/previous-versions/dd743876(v=vs.85)">waveOutWrite</a>, or close the device by calling <a href="/previous-versions/dd743856(v=vs.85)">waveOutClose</a>.

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>