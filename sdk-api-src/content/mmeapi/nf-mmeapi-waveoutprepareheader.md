---
UID: NF:mmeapi.waveOutPrepareHeader
title: waveOutPrepareHeader function (mmeapi.h)
description: The waveOutPrepareHeader function prepares a waveform-audio data block for playback.
helpviewer_keywords: ["_win32_waveOutPrepareHeader","mmsystem/waveOutPrepareHeader","multimedia.waveoutprepareheader","waveOutPrepareHeader","waveOutPrepareHeader function [Windows Multimedia]"]
old-location: multimedia\waveoutprepareheader.htm
tech.root: Multimedia
ms.assetid: f970c7ed-b9c5-45ce-a59b-dee02359ef82
ms.date: 12/05/2018
ms.keywords: _win32_waveOutPrepareHeader, mmsystem/waveOutPrepareHeader, multimedia.waveoutprepareheader, waveOutPrepareHeader, waveOutPrepareHeader function [Windows Multimedia]
req.header: mmeapi.h
req.include-header: Mmeapi.h, Windows.h
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
 - waveOutPrepareHeader
 - mmeapi/waveOutPrepareHeader
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
 - waveOutPrepareHeader
---

# waveOutPrepareHeader function


## -description

The <b>waveOutPrepareHeader</b> function prepares a waveform-audio data block for playback.

## -parameters

### -param hwo

Handle to the waveform-audio output device.

### -param pwh

Pointer to a <a href="/previous-versions/dd743837(v=vs.85)">WAVEHDR</a> structure that identifies the data block to be prepared.

### -param cbwh

Size, in bytes, of the <a href="/previous-versions/dd743837(v=vs.85)">WAVEHDR</a> structure.

## -returns

Returns <b>MMSYSERR_NOERROR</b> if successful or an error otherwise. Possible error values include the following.

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
</table>

## -remarks

Set the <b>lpData</b>, <b>dwBufferLength</b>, and <b>dwFlags</b> members of the <a href="/previous-versions/dd743837(v=vs.85)">WAVEHDR</a> structure before calling this function. Set the <b>dwFlags</b> member to zero.

The <b>dwFlags</b>, <b>dwBufferLength</b>, and <b>dwLoops</b> members of the <a href="/previous-versions/dd743837(v=vs.85)">WAVEHDR</a> structure can change between calls to this function and the <a href="/previous-versions/dd743876(v=vs.85)">waveOutWrite</a> function. If you change the size specified by <b>dwBufferLength</b> before the call to <b>waveOutWrite</b>, the new value must be less than the prepared value.

If the method succeeds, the <b>WHDR_PREPARED</b> flag is set in the <b>dwFlags</b> member of the <a href="/previous-versions/dd743837(v=vs.85)">WAVEHDR</a> structure.

Preparing a header that has already been prepared has no effect, and the function returns zero.

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>