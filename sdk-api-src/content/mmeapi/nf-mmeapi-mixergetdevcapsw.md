---
UID: NF:mmeapi.mixerGetDevCapsW
title: mixerGetDevCapsW function (mmeapi.h)
description: The mixerGetDevCapsW (Unicode) function (mmeapi.h) queries a specified mixer device to determine its capabilities.
helpviewer_keywords: ["_win32_mixerGetDevCaps", "mixerGetDevCaps", "mixerGetDevCaps function [Windows Multimedia]", "mixerGetDevCapsW", "mmeapi/mixerGetDevCaps", "mmeapi/mixerGetDevCapsW", "multimedia.mixergetdevcaps"]
old-location: multimedia\mixergetdevcaps.htm
tech.root: Multimedia
ms.assetid: e3403be8-f3a8-4aab-8498-0556585bc4dd
ms.date: 08/05/2022
ms.keywords: _win32_mixerGetDevCaps, mixerGetDevCaps, mixerGetDevCaps function [Windows Multimedia], mixerGetDevCapsA, mixerGetDevCapsW, mmeapi/mixerGetDevCaps, mmeapi/mixerGetDevCapsA, mmeapi/mixerGetDevCapsW, multimedia.mixergetdevcaps
req.header: mmeapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: mixerGetDevCapsW (Unicode) and mixerGetDevCapsA (ANSI)
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
 - mixerGetDevCapsW
 - mmeapi/mixerGetDevCapsW
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
 - mixerGetDevCaps
 - mixerGetDevCapsA
 - mixerGetDevCapsW
---

# mixerGetDevCapsW function


## -description

The <b>mixerGetDevCaps</b> function queries a specified mixer device to determine its capabilities.

## -parameters

### -param uMxId

Identifier or handle of an open mixer device.

### -param pmxcaps

Pointer to a <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercapsa">MIXERCAPS</a> structure that receives information about the capabilities of the device.

### -param cbmxcaps

Size, in bytes, of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercapsa">MIXERCAPS</a> structure.

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
The specified device identifier is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The mixer device handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>

## -remarks

Use the <a href="/previous-versions/dd757304(v=vs.85)">mixerGetNumDevs</a> function to determine the number of mixer devices present in the system. The device identifier specified by <i>uMxId</i> varies from zero to one less than the number of mixer devices present.

Only the number of bytes (or less) of information specified in <i>cbmxcaps</i> is copied to the location pointed to by <i>pmxcaps</i>. If <i>cbmxcaps</i> is zero, nothing is copied, and the function returns successfully.

This function also accepts a mixer device handle returned by the <a href="/previous-versions/dd757308(v=vs.85)">mixerOpen</a> function as the <i>uMxId</i> parameter. The application should cast the <b>HMIXER</b> handle to a <b>UINT</b>.





> [!NOTE]
> The mmeapi.h header defines mixerGetDevCaps as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/audio-mixer-functions">Audio Mixer Functions</a>



<a href="/windows/desktop/Multimedia/audio-mixers">Audio Mixers</a>
