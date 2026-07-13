---
UID: NS:mmeapi.wavehdr_tag
title: WAVEHDR (mmeapi.h)
description: The WAVEHDR structure defines the header used to identify a waveform-audio buffer.
helpviewer_keywords: ["*LPWAVEHDR","*NPWAVEHDR","*PWAVEHDR","LPWAVEHDR","LPWAVEHDR structure pointer [Windows Multimedia]","WAVEHDR","WAVEHDR structure [Windows Multimedia]","WHDR_BEGINLOOP","WHDR_DONE","WHDR_ENDLOOP","WHDR_INQUEUE","WHDR_PREPARED","_win32_WAVEHDR_str","mmeapi/LPWAVEHDR","mmeapi/WAVEHDR","multimedia.wavehdr","wavehdr_tag"]
old-location: multimedia\wavehdr.htm
tech.root: Multimedia
ms.assetid: be70ae8e-8d8f-4261-bd0e-c6fd7feec520
ms.date: 12/05/2018
ms.keywords: '*LPWAVEHDR, *NPWAVEHDR, *PWAVEHDR, LPWAVEHDR, LPWAVEHDR structure pointer [Windows Multimedia], WAVEHDR, WAVEHDR structure [Windows Multimedia], WHDR_BEGINLOOP, WHDR_DONE, WHDR_ENDLOOP, WHDR_INQUEUE, WHDR_PREPARED, _win32_WAVEHDR_str, mmeapi/LPWAVEHDR, mmeapi/WAVEHDR, multimedia.wavehdr, wavehdr_tag'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WAVEHDR, *PWAVEHDR, *NPWAVEHDR, *LPWAVEHDR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - wavehdr_tag
 - mmeapi/wavehdr_tag
 - PWAVEHDR
 - mmeapi/PWAVEHDR
 - WAVEHDR
 - mmeapi/WAVEHDR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmeapi.h
api_name:
 - WAVEHDR
---

# WAVEHDR structure


## -description

The <b>WAVEHDR</b> structure defines the header used to identify a waveform-audio buffer.

## -struct-fields

### -field lpData

Pointer to the waveform buffer.

### -field dwBufferLength

Length, in bytes, of the buffer.

### -field dwBytesRecorded

When the header is used in input, specifies how much data is in the buffer.

### -field dwUser

User data.

### -field dwFlags

A bitwise <b>OR</b> of zero or more flags. The following flags are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="WHDR_BEGINLOOP"></a><a id="whdr_beginloop"></a><dl>
<dt><b>WHDR_BEGINLOOP</b></dt>
</dl>
</td>
<td width="60%">
This buffer is the first buffer in a loop. This flag is used only with output buffers.

</td>
</tr>
<tr>
<td width="40%"><a id="WHDR_DONE"></a><a id="whdr_done"></a><dl>
<dt><b>WHDR_DONE</b></dt>
</dl>
</td>
<td width="60%">
Set by the device driver to indicate that it is finished with the buffer and is returning it to the application.

</td>
</tr>
<tr>
<td width="40%"><a id="WHDR_ENDLOOP"></a><a id="whdr_endloop"></a><dl>
<dt><b>WHDR_ENDLOOP</b></dt>
</dl>
</td>
<td width="60%">
This buffer is the last buffer in a loop. This flag is used only with output buffers.

</td>
</tr>
<tr>
<td width="40%"><a id="WHDR_INQUEUE"></a><a id="whdr_inqueue"></a><dl>
<dt><b>WHDR_INQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Set by Windows to indicate that the buffer is queued for playback.

</td>
</tr>
<tr>
<td width="40%"><a id="WHDR_PREPARED"></a><a id="whdr_prepared"></a><dl>
<dt><b>WHDR_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
Set by Windows to indicate that the buffer has been prepared with the <a href="/previous-versions/dd743848(v=vs.85)">waveInPrepareHeader</a> or <a href="/previous-versions/dd743868(v=vs.85)">waveOutPrepareHeader</a> function.

</td>
</tr>
</table>

### -field dwLoops

Number of times to play the loop. This member is used only with output buffers.

### -field lpNext

Reserved.

### -field reserved

Reserved.

## -remarks

Use the WHDR_BEGINLOOP and WHDR_ENDLOOP flags in the <b>dwFlags</b> member to specify the beginning and ending data blocks for looping. To loop on a single block, specify both flags for the same block. Use the <b>dwLoops</b> member in the <b>WAVEHDR</b> structure for the first block in the loop to specify the number of times to play the loop.

The <b>lpData</b>, <b>dwBufferLength</b>, and <b>dwFlags</b> members must be set before calling the <a href="/previous-versions/dd743848(v=vs.85)">waveInPrepareHeader</a> or <a href="/previous-versions/dd743868(v=vs.85)">waveOutPrepareHeader</a> function. (For either function, the <b>dwFlags</b> member must be set to zero.)

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-structures">Waveform Structures</a>



<a href="/previous-versions/dd743848(v=vs.85)">waveInPrepareHeader</a>



<a href="/previous-versions/dd743868(v=vs.85)">waveOutPrepareHeader</a>
