---
UID: NS:vfw._AVIFILEINFOA
title: AVIFILEINFOA (vfw.h)
description: The AVIFILEINFO structure contains global information for an entire AVI file. (ANSI)
helpviewer_keywords: ["*LPAVIFILEINFOA","AVIFILECAPS_ALLKEYFRAMES","AVIFILECAPS_CANREAD","AVIFILECAPS_CANWRITE","AVIFILECAPS_NOCOMPRESSION","AVIFILEINFO","AVIFILEINFO structure [Windows Multimedia]","AVIFILEINFOA","AVIFILEINFOW","AVIFILEINFO_COPYRIGHTED","AVIFILEINFO_HASINDEX","AVIFILEINFO_ISINTERLEAVED","AVIFILEINFO_MUSTUSEINDEX","AVIFILEINFO_WASCAPTUREFILE","multimedia.avifileinfo_COLLISION510","multimedia.avifileinfo_struct","vfw/AVIFILEINFO"]
old-location: multimedia\avifileinfo_struct.htm
tech.root: Multimedia
ms.assetid: d3fda342-2ade-41b1-b709-c194f132e015
ms.date: 12/05/2018
ms.keywords: '*LPAVIFILEINFOA, AVIFILECAPS_ALLKEYFRAMES, AVIFILECAPS_CANREAD, AVIFILECAPS_CANWRITE, AVIFILECAPS_NOCOMPRESSION, AVIFILEINFO, AVIFILEINFO structure [Windows Multimedia], AVIFILEINFOA, AVIFILEINFOW, AVIFILEINFO_COPYRIGHTED, AVIFILEINFO_HASINDEX, AVIFILEINFO_ISINTERLEAVED, AVIFILEINFO_MUSTUSEINDEX, AVIFILEINFO_WASCAPTUREFILE, multimedia.avifileinfo_COLLISION510, multimedia.avifileinfo_struct, vfw/AVIFILEINFO'
req.header: vfw.h
req.include-header: 
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
req.typenames: AVIFILEINFOA, *LPAVIFILEINFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AVIFILEINFOA
 - vfw/_AVIFILEINFOA
 - LPAVIFILEINFOA
 - vfw/LPAVIFILEINFOA
 - AVIFILEINFOA
 - vfw/AVIFILEINFOA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - AVIFILEINFO
---

# AVIFILEINFOA structure


## -description

The <b>AVIFILEINFO</b> structure contains global information for an entire AVI file.

## -struct-fields

### -field dwMaxBytesPerSec

Approximate maximum data rate of the AVI file.

### -field dwFlags

A bitwise <b>OR</b> of zero or more flags. The following flags are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="AVIFILEINFO_HASINDEX"></a><a id="avifileinfo_hasindex"></a><dl>
<dt><b>AVIFILEINFO_HASINDEX</b></dt>
</dl>
</td>
<td width="60%">
The AVI file has an index at the end of the file. For good performance, all AVI files should contain an index.

</td>
</tr>
<tr>
<td width="40%"><a id="AVIFILEINFO_MUSTUSEINDEX"></a><a id="avifileinfo_mustuseindex"></a><dl>
<dt><b>AVIFILEINFO_MUSTUSEINDEX</b></dt>
</dl>
</td>
<td width="60%">
The file index contains the playback order for the chunks in the file. Use the index rather than the physical ordering of the chunks when playing back the data. This could be used for creating a list of frames for editing.

</td>
</tr>
<tr>
<td width="40%"><a id="AVIFILEINFO_ISINTERLEAVED"></a><a id="avifileinfo_isinterleaved"></a><dl>
<dt><b>AVIFILEINFO_ISINTERLEAVED</b></dt>
</dl>
</td>
<td width="60%">
The AVI file is interleaved.

</td>
</tr>
<tr>
<td width="40%"><a id="AVIFILEINFO_WASCAPTUREFILE"></a><a id="avifileinfo_wascapturefile"></a><dl>
<dt><b>AVIFILEINFO_WASCAPTUREFILE</b></dt>
</dl>
</td>
<td width="60%">
The AVI file is a specially allocated file used for capturing real-time video. Applications should warn the user before writing over a file with this flag set because the user probably defragmented this file.

</td>
</tr>
<tr>
<td width="40%"><a id="AVIFILEINFO_COPYRIGHTED"></a><a id="avifileinfo_copyrighted"></a><dl>
<dt><b>AVIFILEINFO_COPYRIGHTED</b></dt>
</dl>
</td>
<td width="60%">
The AVI file contains copyrighted data and software. When this flag is used, software should not permit the data to be duplicated.

</td>
</tr>
</table>

### -field dwCaps

Capability flags. The following flags are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="AVIFILECAPS_CANREAD"></a><a id="avifilecaps_canread"></a><dl>
<dt><b>AVIFILECAPS_CANREAD</b></dt>
</dl>
</td>
<td width="60%">
An application can open the AVI file with the read privilege.

</td>
</tr>
<tr>
<td width="40%"><a id="AVIFILECAPS_CANWRITE"></a><a id="avifilecaps_canwrite"></a><dl>
<dt><b>AVIFILECAPS_CANWRITE</b></dt>
</dl>
</td>
<td width="60%">
An application can open the AVI file with the write privilege.

</td>
</tr>
<tr>
<td width="40%"><a id="AVIFILECAPS_ALLKEYFRAMES"></a><a id="avifilecaps_allkeyframes"></a><dl>
<dt><b>AVIFILECAPS_ALLKEYFRAMES</b></dt>
</dl>
</td>
<td width="60%">
Every frame in the AVI file is a key frame.

</td>
</tr>
<tr>
<td width="40%"><a id="AVIFILECAPS_NOCOMPRESSION"></a><a id="avifilecaps_nocompression"></a><dl>
<dt><b>AVIFILECAPS_NOCOMPRESSION</b></dt>
</dl>
</td>
<td width="60%">
The AVI file does not use a compression method.

</td>
</tr>
</table>

### -field dwStreams

Number of streams in the file. For example, a file with audio and video has at least two streams.

### -field dwSuggestedBufferSize

Suggested buffer size, in bytes, for reading the file. Generally, this size should be large enough to contain the largest chunk in the file. For an interleaved file, this size should be large enough to read an entire record, not just a chunk.

If the buffer size is too small or is set to zero, the playback software will have to reallocate memory during playback, reducing performance.

### -field dwWidth

Width, in pixels, of the AVI file.

### -field dwHeight

Height, in pixels, of the AVI file.

### -field dwScale

Time scale applicable for the entire file. Dividing <b>dwRate</b> by <b>dwScale</b> gives the number of samples per second.

Any stream can define its own time scale to supersede the file time scale.

### -field dwRate

Rate in an integer format. To obtain the rate in samples per second, divide this value by the value in <b>dwScale</b>.

### -field dwLength

Length of the AVI file. The units are defined by <b>dwRate</b> and <b>dwScale</b>.

### -field dwEditCount

Number of streams that have been added to or deleted from the AVI file.

### -field szFileType

Null-terminated string containing descriptive information for the file type.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/Multimedia/avifile-structures">AVIFile Structures</a>

## -remarks

> [!NOTE]
> The vfw.h header defines AVIFILEINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
