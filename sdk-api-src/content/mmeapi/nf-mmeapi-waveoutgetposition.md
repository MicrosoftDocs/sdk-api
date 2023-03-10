---
UID: NF:mmeapi.waveOutGetPosition
title: waveOutGetPosition function (mmeapi.h)
description: The waveOutGetPosition function retrieves the current playback position of the given waveform-audio output device.
helpviewer_keywords: ["_win32_waveOutGetPosition","mmeapi/waveOutGetPosition","multimedia.waveoutgetposition","waveOutGetPosition","waveOutGetPosition function [Windows Multimedia]"]
old-location: multimedia\waveoutgetposition.htm
tech.root: Multimedia
ms.assetid: 66279da3-0ed7-489b-a465-88e781a8443d
ms.date: 12/05/2018
ms.keywords: _win32_waveOutGetPosition, mmeapi/waveOutGetPosition, multimedia.waveoutgetposition, waveOutGetPosition, waveOutGetPosition function [Windows Multimedia]
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
 - waveOutGetPosition
 - mmeapi/waveOutGetPosition
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
 - waveOutGetPosition
---

# waveOutGetPosition function


## -description

The <b>waveOutGetPosition</b> function retrieves the current playback position of the given waveform-audio output device.

## -parameters

### -param hwo

Handle to the waveform-audio output device.

### -param pmmt

Pointer to an <a href="/previous-versions/dd757347(v=vs.85)">MMTIME</a> structure.

### -param cbmmt

Size, in bytes, of the <b>MMTIME</b> structure.

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

Before calling this function, set the <b>wType</b> member of the <b>MMTIME</b> structure to indicate the time format you want. After calling this function, check <b>wType</b> to determine whether the time format is supported. If the format is not supported, <b>wType</b> will specify an alternative format.

The position is set to zero when the device is opened or reset.

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>