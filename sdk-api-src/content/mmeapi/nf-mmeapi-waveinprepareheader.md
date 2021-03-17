---
UID: NF:mmeapi.waveInPrepareHeader
title: waveInPrepareHeader function (mmeapi.h)
description: The waveInPrepareHeader function prepares a buffer for waveform-audio input.
helpviewer_keywords: ["_win32_waveInPrepareHeader","mmeapi/waveInPrepareHeader","multimedia.waveinprepareheader","waveInPrepareHeader","waveInPrepareHeader function [Windows Multimedia]"]
old-location: multimedia\waveinprepareheader.htm
tech.root: Multimedia
ms.assetid: 2b99eb91-2cc6-4394-af57-4b1276f08974
ms.date: 12/05/2018
ms.keywords: _win32_waveInPrepareHeader, mmeapi/waveInPrepareHeader, multimedia.waveinprepareheader, waveInPrepareHeader, waveInPrepareHeader function [Windows Multimedia]
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
 - waveInPrepareHeader
 - mmeapi/waveInPrepareHeader
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
 - waveInPrepareHeader
---

# waveInPrepareHeader function


## -description

The <b>waveInPrepareHeader</b> function prepares a buffer for waveform-audio input.

## -parameters

### -param hwi

Handle to the waveform-audio input device.

### -param pwh

Pointer to a <a href="/previous-versions/dd743837(v=vs.85)">WAVEHDR</a> structure that identifies the buffer to be prepared.

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
</table>

## -remarks

The <b>lpData</b>, <b>dwBufferLength</b>, and <b>dwFlags</b> members of the <b>WAVEHDR</b> structure must be set before calling this function (<b>dwFlags</b> must be zero).

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>