---
UID: NS:wmsdkidl._WMSynchronisedLyrics
title: WM_SYNCHRONISED_LYRICS (wmsdkidl.h)
description: The WM_SYNCHRONISED_LYRICS structure is used as the data item for the WM/Lyrics_Synchronised complex metadata attribute.
helpviewer_keywords: ["WM_SYNCHRONISED_LYRICS","WM_SYNCHRONISED_LYRICS structure [windows Media Format]","wmformat.wm_synchronised_lyrics","wmsdkidl/WM_SYNCHRONISED_LYRICS"]
old-location: wmformat\wm_synchronised_lyrics.htm
tech.root: wmformat
ms.assetid: a8f47fcc-faf7-4a25-817a-f9199db38fbc
ms.date: 4/26/2023
ms.keywords: WM_SYNCHRONISED_LYRICS, WM_SYNCHRONISED_LYRICS structure [windows Media Format], wmformat.wm_synchronised_lyrics, wmsdkidl/WM_SYNCHRONISED_LYRICS
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.typenames: WM_SYNCHRONISED_LYRICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMSynchronisedLyrics
 - wmsdkidl/_WMSynchronisedLyrics
 - WM_SYNCHRONISED_LYRICS
 - wmsdkidl/WM_SYNCHRONISED_LYRICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WM_SYNCHRONISED_LYRICS
---

# WM_SYNCHRONISED_LYRICS structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WM_SYNCHRONISED_LYRICS</b> structure is used as the data item for the <a href="/windows/desktop/wmformat/wm-lyrics-synchronised">WM/Lyrics_Synchronised</a> complex metadata attribute.

## -struct-fields

### -field bTimeStampFormat

<b>BYTE</b> specifying the format of time stamps in the lyrics. Set to one of the following values.<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>1</td>
<td>Time stamps are 32-bit values containing the absolute time of the lyric in frame numbers.</td>
</tr>
<tr>
<td>2</td>
<td>Time stamps are 32-bit values containing the absolute time of the lyric in milliseconds.</td>
</tr>
</table>

### -field bContentType

<b>BYTE</b> specifying the type of synchronized strings that are in the lyrics data. Set to one of the following values.<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>0</td>
<td>Synchronized strings other than the types listed in this table</td>
</tr>
<tr>
<td>1</td>
<td>Song lyrics</td>
</tr>
<tr>
<td>2</td>
<td>Text transcription</td>
</tr>
<tr>
<td>3</td>
<td>Names of parts of the content. For example, movements of classical pieces, like "Adagio"</td>
</tr>
<tr>
<td>4</td>
<td>Events, such as stage directions in operas</td>
</tr>
<tr>
<td>5</td>
<td>Chord notations</td>
</tr>
<tr>
<td>6</td>
<td>Trivia information</td>
</tr>
<tr>
<td>7</td>
<td>URLs to Web pages</td>
</tr>
<tr>
<td>8</td>
<td>URLs to images</td>
</tr>
</table>

### -field pwszContentDescriptor

Pointer to a wide-character null-terminated string containing data from the encoding application. An individual application can use this member in any way desired.

### -field dwLyricsLen

<b>DWORD</b> containing the length, in bytes, of the lyric data pointed to by <b>pbLyrics</b>.

### -field pbLyrics

Pointer to a <b>BYTE</b> array containing the lyrics. You can break the lyrics into syllables, or divide them in some other way that suits the needs of your application. Each syllable or part is included as a null-terminated, wide-character string followed by a 32-bit time stamp. The unit of measurement for the time stamp is determined by the value of <b>bTimeStampFormat</b>.

## -remarks

The objects of the Windows Media Format SDK do not validate the values of time stamps for synchronized lyrics. However, the data is checked to ensure that there is a time stamp for every string, and that the data alternates between strings and integers.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>