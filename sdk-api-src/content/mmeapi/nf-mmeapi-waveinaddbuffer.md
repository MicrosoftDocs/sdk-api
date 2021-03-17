---
UID: NF:mmeapi.waveInAddBuffer
title: waveInAddBuffer function (mmeapi.h)
description: The waveInAddBuffer function sends an input buffer to the given waveform-audio input device. When the buffer is filled, the application is notified.
helpviewer_keywords: ["_win32_waveInAddBuffer","mmeapi/waveInAddBuffer","multimedia.waveinaddbuffer","waveInAddBuffer","waveInAddBuffer function [Windows Multimedia]"]
old-location: multimedia\waveinaddbuffer.htm
tech.root: Multimedia
ms.assetid: 343abdb6-7a0f-4756-9920-60d308e845f9
ms.date: 12/05/2018
ms.keywords: _win32_waveInAddBuffer, mmeapi/waveInAddBuffer, multimedia.waveinaddbuffer, waveInAddBuffer, waveInAddBuffer function [Windows Multimedia]
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
 - waveInAddBuffer
 - mmeapi/waveInAddBuffer
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
 - waveInAddBuffer
---

# waveInAddBuffer function


## -description

The <b>waveInAddBuffer</b> function sends an input buffer to the given waveform-audio input device. When the buffer is filled, the application is notified.

## -parameters

### -param hwi

Handle to the waveform-audio input device.

### -param pwh

Pointer to a <a href="/previous-versions/dd743837(v=vs.85)">WAVEHDR</a> structure that identifies the buffer.

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
The buffer pointed to by the <i>pwh</i> parameter hasn't been prepared.

</td>
</tr>
</table>

## -remarks

When the buffer is filled, the WHDR_DONE bit is set in the <b>dwFlags</b> member of the <b>WAVEHDR</b> structure.

The buffer must be prepared with the <b>waveInPrepareHeader</b> function before it is passed to this function.

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>