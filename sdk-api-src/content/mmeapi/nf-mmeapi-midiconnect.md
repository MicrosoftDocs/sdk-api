---
UID: NF:mmeapi.midiConnect
title: midiConnect function (mmeapi.h)
description: The midiConnect function connects a MIDI input device to a MIDI thru or output device, or connects a MIDI thru device to a MIDI output device.
helpviewer_keywords: ["_win32_midiConnect","midiConnect","midiConnect function [Windows Multimedia]","mmeapi/midiConnect","multimedia.midiconnect"]
old-location: multimedia\midiconnect.htm
tech.root: Multimedia
ms.assetid: 24ee806a-f8a2-470e-8737-e4e5216f2705
ms.date: 12/05/2018
ms.keywords: _win32_midiConnect, midiConnect, midiConnect function [Windows Multimedia], mmeapi/midiConnect, multimedia.midiconnect
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
 - midiConnect
 - mmeapi/midiConnect
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
 - midiConnect
---

# midiConnect function


## -description

The <b>midiConnect</b> function connects a MIDI input device to a MIDI thru or output device, or connects a MIDI thru device to a MIDI output device.

## -parameters

### -param hmi

Handle to a MIDI input device or a MIDI thru device. (For thru devices, this handle must have been returned by a call to the <a href="/previous-versions/dd798476(v=vs.85)">midiOutOpen</a> function.)

### -param hmo

Handle to the MIDI output or thru device.

### -param pReserved

Reserved; must be <b>NULL</b>.

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
<dt><b>MIDIERR_NOTREADY</b></dt>
</dl>
</td>
<td width="60%">
Specified input device is already connected to an output device.

</td>
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
</table>

## -remarks

After calling this function, the MIDI input device receives event data in an MIM_DATA message whenever a message with the same event data is sent to the output device driver.

A thru driver is a special form of MIDI output driver. The system will allow only one MIDI output device to be connected to a MIDI input device, but multiple MIDI output devices can be connected to a MIDI thru device. Whenever the given MIDI input device receives event data in an MIM_DATA message, a message with the same event data is sent to the given output device driver (or through the thru driver to the output drivers).

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>