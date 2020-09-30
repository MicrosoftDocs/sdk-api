---
UID: NF:mmeapi.auxGetVolume
title: auxGetVolume function (mmeapi.h)
description: The auxGetVolume function retrieves the current volume setting of the specified auxiliary output device.
helpviewer_keywords: ["_win32_auxGetVolume","auxGetVolume","auxGetVolume function [Windows Multimedia]","mmeapi/auxGetVolume","multimedia.auxgetvolume"]
old-location: multimedia\auxgetvolume.htm
tech.root: Multimedia
ms.assetid: a427cdb5-83ec-4529-847d-1494118ef926
ms.date: 12/05/2018
ms.keywords: _win32_auxGetVolume, auxGetVolume, auxGetVolume function [Windows Multimedia], mmeapi/auxGetVolume, multimedia.auxgetvolume
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
 - auxGetVolume
 - mmeapi/auxGetVolume
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
 - auxGetVolume
---

# auxGetVolume function


## -description

The <b>auxGetVolume</b> function retrieves the current volume setting of the specified auxiliary output device.

## -parameters

### -param uDeviceID

Identifier of the auxiliary output device to be queried.

### -param pdwVolume

Pointer to a variable to be filled with the current volume setting. The low-order word of this location contains the left channel volume setting, and the high-order word contains the right channel setting. A value of 0xFFFF represents full volume, and a value of 0x0000 is silence.

If a device does not support both left and right volume control, the low-order word of the specified location contains the volume level.

The full 16-bit setting(s) set with the <a href="/previous-versions/dd756717(v=vs.85)">auxSetVolume</a> function are returned, regardless of whether the device supports the full 16 bits of volume-level control.

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
<dt><b>MMSYSERR_BADDEVICEID</b></dt>
</dl>
</td>
<td width="60%">
Specified device identifier is out of range.

</td>
</tr>
</table>

## -remarks

Not all devices support volume control. To determine whether a device supports volume control, use the AUXCAPS_VOLUME flag to test the <b>dwSupport</b> member of the <a href="/previous-versions/dd756711(v=vs.85)">AUXCAPS</a> structure (filled by the <a href="/previous-versions/dd756712(v=vs.85)">auxGetDevCaps</a> function).

To determine whether a device supports volume control on both the left and right channels, use the AUXCAPS_LRVOLUME flag to test the <b>dwSupport</b> member of the <a href="/previous-versions/dd756711(v=vs.85)">AUXCAPS</a> structure (filled by <a href="/previous-versions/dd756712(v=vs.85)">auxGetDevCaps</a>).

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>