---
UID: NF:mmeapi.auxSetVolume
title: auxSetVolume function (mmeapi.h)
description: The auxSetVolume function sets the volume of the specified auxiliary output device.
helpviewer_keywords: ["_win32_auxSetVolume","auxSetVolume","auxSetVolume function [Windows Multimedia]","mmeapi/auxSetVolume","multimedia.auxsetvolume"]
old-location: multimedia\auxsetvolume.htm
tech.root: Multimedia
ms.assetid: 886acacd-f2ac-4e75-aa3d-668e6d4fbbf2
ms.date: 12/05/2018
ms.keywords: _win32_auxSetVolume, auxSetVolume, auxSetVolume function [Windows Multimedia], mmeapi/auxSetVolume, multimedia.auxsetvolume
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
 - auxSetVolume
 - mmeapi/auxSetVolume
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
 - auxSetVolume
---

# auxSetVolume function


## -description

The <b>auxSetVolume</b> function sets the volume of the specified auxiliary output device.

## -parameters

### -param uDeviceID

Identifier of the auxiliary output device to be queried. Device identifiers are determined implicitly from the number of devices present in the system. Device identifier values range from zero to one less than the number of devices present. Use the <a href="/previous-versions/dd756713(v=vs.85)">auxGetNumDevs</a> function to determine the number of auxiliary devices in the system.

### -param dwVolume

Specifies the new volume setting. The low-order word specifies the left-channel volume setting, and the high-order word specifies the right-channel setting. A value of 0xFFFF represents full volume, and a value of 0x0000 is silence.

If a device does not support both left and right volume control, the low-order word of <i>dwVolume</i> specifies the volume level, and the high-order word is ignored.

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

Not all devices support volume control. To determine whether the device supports volume control, use the AUXCAPS_VOLUME flag to test the <b>dwSupport</b> member of the <a href="/previous-versions/dd756711(v=vs.85)">AUXCAPS</a> structure (filled by the <a href="/previous-versions/dd756712(v=vs.85)">auxGetDevCaps</a> function).

To determine whether the device supports volume control on both the left and right channels, use the AUXCAPS_LRVOLUME flag to test the <b>dwSupport</b> member of the <a href="/previous-versions/dd756711(v=vs.85)">AUXCAPS</a> structure (filled by <a href="/previous-versions/dd756712(v=vs.85)">auxGetDevCaps</a>).

Most devices do not support the full 16 bits of volume-level control and will use only the high-order bits of the requested volume setting. For example, for a device that supports 4 bits of volume control, requested volume level values of 0x4000, 0x4FFF, and 0x43BE will produce the same physical volume setting, 0x4000. The <a href="/previous-versions/dd756714(v=vs.85)">auxGetVolume</a> function will return the full 16-bit setting set with <b>auxSetVolume</b>.

Volume settings are interpreted logarithmically. This means the perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>