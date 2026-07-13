---
UID: NF:mmeapi.midiOutGetErrorTextA
title: midiOutGetErrorTextA function (mmeapi.h)
description: The midiOutGetErrorText function retrieves a textual description for an error identified by the specified error code. (midiOutGetErrorTextA)
helpviewer_keywords: ["midiOutGetErrorTextA", "mmeapi/midiOutGetErrorTextA"]
old-location: multimedia\midioutgeterrortext.htm
tech.root: Multimedia
ms.assetid: e0e9a22f-da8b-4c87-bbdb-dedc22336503
ms.date: 12/05/2018
ms.keywords: _win32_midiOutGetErrorText, midiOutGetErrorText, midiOutGetErrorText function [Windows Multimedia], midiOutGetErrorTextA, midiOutGetErrorTextW, mmeapi/midiOutGetErrorText, mmeapi/midiOutGetErrorTextA, mmeapi/midiOutGetErrorTextW, multimedia.midioutgeterrortext
req.header: mmeapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: midiOutGetErrorTextW (Unicode) and midiOutGetErrorTextA (ANSI)
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
 - midiOutGetErrorTextA
 - mmeapi/midiOutGetErrorTextA
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
 - midiOutGetErrorText
 - midiOutGetErrorTextA
 - midiOutGetErrorTextW
---

# midiOutGetErrorTextA function


## -description

The <b>midiOutGetErrorText</b> function retrieves a textual description for an error identified by the specified error code.

## -parameters

### -param mmrError

Error code.

### -param pszText

Pointer to a buffer to be filled with the textual error description.

### -param cchText

Length, in characters, of the buffer pointed to by <i>lpText</i>.

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
<dt><b>MMSYSERR_BADERRNUM</b></dt>
</dl>
</td>
<td width="60%">
The specified error number is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
The specified pointer or structure is invalid.

</td>
</tr>
</table>

## -remarks

If the textual error description is longer than the specified buffer, the description is truncated. The returned error string is always null-terminated. If <i>cchText</i> is zero, nothing is copied, and the function returns MMSYSERR_NOERROR. All error descriptions are less than MAXERRORLENGTH characters long.





> [!NOTE]
> The mmeapi.h header defines midiOutGetErrorText as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>
