---
UID: NF:mmeapi.waveInClose
title: waveInClose function (mmeapi.h)
description: The waveInClose function closes the given waveform-audio input device.
helpviewer_keywords: ["_win32_waveInClose","mmeapi/waveInClose","multimedia.waveinclose","waveInClose","waveInClose function [Windows Multimedia]"]
old-location: multimedia\waveinclose.htm
tech.root: Multimedia
ms.assetid: e064edee-7b13-4fbe-8be9-a8bdfc1cae79
ms.date: 12/05/2018
ms.keywords: _win32_waveInClose, mmeapi/waveInClose, multimedia.waveinclose, waveInClose, waveInClose function [Windows Multimedia]
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
 - waveInClose
 - mmeapi/waveInClose
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
 - waveInClose
---

# waveInClose function


## -description

The <b>waveInClose</b> function closes the given waveform-audio input device.

## -parameters

### -param hwi

Handle to the waveform-audio input device. If the function succeeds, the handle is no longer valid after this call.

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
There are still buffers in the queue.

</td>
</tr>
</table>

## -remarks

If there are input buffers that have been sent with the <b>waveInAddBuffer</b> function and that haven't been returned to the application, the close operation will fail. Call the <b>waveInReset</b> function to mark all pending buffers as done.

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>