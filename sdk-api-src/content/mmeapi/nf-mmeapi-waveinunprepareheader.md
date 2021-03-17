---
UID: NF:mmeapi.waveInUnprepareHeader
title: waveInUnprepareHeader function (mmeapi.h)
description: The waveInUnprepareHeader function cleans up the preparation performed by the waveInPrepareHeader function.
helpviewer_keywords: ["_win32_waveInUnprepareHeader","mmeapi/waveInUnprepareHeader","multimedia.waveinunprepareheader","waveInUnprepareHeader","waveInUnprepareHeader function [Windows Multimedia]"]
old-location: multimedia\waveinunprepareheader.htm
tech.root: Multimedia
ms.assetid: 13222b09-c58b-461d-85b7-9312a03a888a
ms.date: 12/05/2018
ms.keywords: _win32_waveInUnprepareHeader, mmeapi/waveInUnprepareHeader, multimedia.waveinunprepareheader, waveInUnprepareHeader, waveInUnprepareHeader function [Windows Multimedia]
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
 - waveInUnprepareHeader
 - mmeapi/waveInUnprepareHeader
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
 - waveInUnprepareHeader
---

# waveInUnprepareHeader function


## -description

The <b>waveInUnprepareHeader</b> function cleans up the preparation performed by the <a href="/previous-versions/dd743848(v=vs.85)">waveInPrepareHeader</a> function. This function must be called after the device driver fills a buffer and returns it to the application. You must call this function before freeing the buffer.

## -parameters

### -param hwi

Handle to the waveform-audio input device.

### -param pwh

Pointer to a <a href="/previous-versions/dd743837(v=vs.85)">WAVEHDR</a> structure identifying the buffer to be cleaned up.

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
<dt><b>WAVERR_STILLPLAYING</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>pwh</i> parameter is still in the queue.

</td>
</tr>
</table>

## -remarks

This function complements the <b>waveInPrepareHeader</b> function.

You must call this function before freeing the buffer. After passing a buffer to the device driver with the <b>waveInAddBuffer</b> function, you must wait until the driver is finished with the buffer before calling <b>waveInUnprepareHeader</b>. Unpreparing a buffer that has not been prepared has no effect, and the function returns zero.

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>