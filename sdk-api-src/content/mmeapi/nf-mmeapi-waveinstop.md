---
UID: NF:mmeapi.waveInStop
title: waveInStop function (mmeapi.h)
description: The waveInStop function stops waveform-audio input.
helpviewer_keywords: ["_win32_waveInStop","mmeapi/waveInStop","multimedia.waveinstop","waveInStop","waveInStop function [Windows Multimedia]"]
old-location: multimedia\waveinstop.htm
tech.root: Multimedia
ms.assetid: c56085f9-256d-41e2-a3d5-7d17d42f0e57
ms.date: 12/05/2018
ms.keywords: _win32_waveInStop, mmeapi/waveInStop, multimedia.waveinstop, waveInStop, waveInStop function [Windows Multimedia]
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
 - waveInStop
 - mmeapi/waveInStop
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
 - waveInStop
---

# waveInStop function


## -description

The <b>waveInStop</b> function stops waveform-audio input.

## -parameters

### -param hwi

Handle to the waveform-audio input device.

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

If there are any buffers in the queue, the current buffer will be marked as done (the <b>dwBytesRecorded</b> member in the header will contain the length of data), but any empty buffers in the queue will remain there.

Calling this function when input is not started has no effect, and the function returns zero.

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>