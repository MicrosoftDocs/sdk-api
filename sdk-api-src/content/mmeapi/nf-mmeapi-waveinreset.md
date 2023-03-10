---
UID: NF:mmeapi.waveInReset
title: waveInReset function (mmeapi.h)
description: The waveInReset function stops input on the given waveform-audio input device and resets the current position to zero. All pending buffers are marked as done and returned to the application.
helpviewer_keywords: ["_win32_waveInReset","mmeapi/waveInReset","multimedia.waveinreset","waveInReset","waveInReset function [Windows Multimedia]"]
old-location: multimedia\waveinreset.htm
tech.root: Multimedia
ms.assetid: 3f0735ec-3a0a-478d-8044-8a8671cf2d5c
ms.date: 12/05/2018
ms.keywords: _win32_waveInReset, mmeapi/waveInReset, multimedia.waveinreset, waveInReset, waveInReset function [Windows Multimedia]
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
 - waveInReset
 - mmeapi/waveInReset
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
 - waveInReset
---

# waveInReset function


## -description

The <b>waveInReset</b> function stops input on the given waveform-audio input device and resets the current position to zero. All pending buffers are marked as done and returned to the application.

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

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>