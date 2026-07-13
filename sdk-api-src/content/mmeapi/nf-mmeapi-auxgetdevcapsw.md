---
UID: NF:mmeapi.auxGetDevCapsW
title: auxGetDevCapsW function (mmeapi.h)
description: The auxGetDevCapsW (Unicode) function (mmeapi.h) retrieves the capabilities of a given auxiliary output device.
helpviewer_keywords: ["_win32_auxGetDevCaps", "auxGetDevCaps", "auxGetDevCaps function [Windows Multimedia]", "auxGetDevCapsW", "mmeapi/auxGetDevCaps", "mmeapi/auxGetDevCapsW", "multimedia.auxgetdevcaps"]
old-location: multimedia\auxgetdevcaps.htm
tech.root: Multimedia
ms.assetid: c0920425-fb42-4112-b0c1-f4b607b9e794
ms.date: 08/05/2022
ms.keywords: _win32_auxGetDevCaps, auxGetDevCaps, auxGetDevCaps function [Windows Multimedia], auxGetDevCapsA, auxGetDevCapsW, mmeapi/auxGetDevCaps, mmeapi/auxGetDevCapsA, mmeapi/auxGetDevCapsW, multimedia.auxgetdevcaps
req.header: mmeapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: auxGetDevCapsW (Unicode) and auxGetDevCapsA (ANSI)
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
 - auxGetDevCapsW
 - mmeapi/auxGetDevCapsW
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
 - auxGetDevCaps
 - auxGetDevCapsA
 - auxGetDevCapsW
---

# auxGetDevCapsW function


## -description

The <b>auxGetDevCaps</b> function retrieves the capabilities of a given auxiliary output device.

## -parameters

### -param uDeviceID

Identifier of the auxiliary output device to be queried. Specify a valid device identifier (see the following comments section), or use the following constant:

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>AUX_MAPPER</td>
<td>Auxiliary audio mapper. The function returns an error if no auxiliary audio mapper is installed.</td>
</tr>
</table>

### -param pac

Pointer to an <a href="/previous-versions/dd756711(v=vs.85)">AUXCAPS</a> structure to be filled with information about the capabilities of the device.

### -param cbac

Size, in bytes, of the <a href="/previous-versions/dd756711(v=vs.85)">AUXCAPS</a> structure.

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

The device identifier in <i>uDeviceID</i> varies from zero to one less than the number of devices present. AUX_MAPPER may also be used. Use the <a href="/previous-versions/dd756713(v=vs.85)">auxGetNumDevs</a> function to determine the number of auxiliary output devices present in the system.





> [!NOTE]
> The mmeapi.h header defines auxGetDevCaps as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>
