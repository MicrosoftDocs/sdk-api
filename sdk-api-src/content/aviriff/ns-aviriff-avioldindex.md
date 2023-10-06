---
UID: NS:aviriff._avioldindex
title: AVIOLDINDEX (aviriff.h)
description: The AVIOLDINDEX structure describes an AVI 1.0 index ('idx1' format). New AVI files should use an AVI 2.0 index ('indx' format).
helpviewer_keywords: ["AVIIF_KEYFRAME","AVIIF_LIST","AVIIF_NO_TIME","AVIOLDINDEX","AVIOLDINDEX structure [DirectShow]","AVIOLDINDEXStructure","aviriff/AVIOLDINDEX","db","dc","dshow.avioldindex","pc","wb"]
old-location: dshow\avioldindex.htm
tech.root: DirectShow
ms.assetid: c36d5759-710e-4abe-85dc-13462013bb9f
ms.date: 4/26/2023
ms.keywords: AVIIF_KEYFRAME, AVIIF_LIST, AVIIF_NO_TIME, AVIOLDINDEX, AVIOLDINDEX structure [DirectShow], AVIOLDINDEXStructure, aviriff/AVIOLDINDEX, db, dc, dshow.avioldindex, pc, wb
req.header: aviriff.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: AVIOLDINDEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _avioldindex
 - aviriff/_avioldindex
 - AVIOLDINDEX
 - aviriff/AVIOLDINDEX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Aviriff.h
api_name:
 - AVIOLDINDEX
---

# AVIOLDINDEX structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AVIOLDINDEX</b> structure describes an AVI 1.0 index ('idx1' format). New AVI files should use an AVI 2.0 index ('indx' format).

## -struct-fields

### -field fcc

Specifies a FOURCC code. The value must be 'idx1'.

### -field cb

Specifies the size of the structure, not including the initial 8 bytes.

### -field _avioldindex_entry

### -field _avioldindex_entry.dwChunkId

### -field _avioldindex_entry.dwFlags

### -field _avioldindex_entry.dwOffset

### -field _avioldindex_entry.dwSize

### -field aIndex

Array of structures that contain the following members.



#### dwChunkId

Specifies a FOURCC that identifies a stream in the AVI file. The FOURCC must have the form 'xxyy' where <i>xx</i> is the stream number and <i>yy</i> is a two-character code that identifies the contents of the stream:



##### db (Uncompressed video frame)



##### dc (Compressed video frame)



##### pc (Palette change)



##### wb (Audio data)



#### dwFlags

Specifies a bitwise combination of zero or more of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AVIIF_KEYFRAME"></a><a id="aviif_keyframe"></a><dl>
<dt><b>AVIIF_KEYFRAME</b></dt>
</dl>
</td>
<td width="60%">
The data chunk is a key frame.

</td>
</tr>
<tr>
<td width="40%"><a id="AVIIF_LIST"></a><a id="aviif_list"></a><dl>
<dt><b>AVIIF_LIST</b></dt>
</dl>
</td>
<td width="60%">
The data chunk is a 'rec ' list.

</td>
</tr>
<tr>
<td width="40%"><a id="AVIIF_NO_TIME"></a><a id="aviif_no_time"></a><dl>
<dt><b>AVIIF_NO_TIME</b></dt>
</dl>
</td>
<td width="60%">
The data chunk does not affect the timing of the stream. For example, this flag should be set for palette changes.

</td>
</tr>
</table>
 



#### dwOffset

Specifies the location of the data chunk in the file. The value should be specified as an offset, in bytes, from the start of the 'movi' list; however, in some AVI files it is given as an offset from the start of the file.



#### dwSize

Specifies the size of the data chunk, in bytes.

## -remarks

This structure consists of the initial RIFF chunk (the <b>fcc</b> and <b>cb</b> members) followed by one index entry for each data chunk in the 'movi' list.

## -see-also

<a href="/windows/desktop/DirectShow/avi-riff-file-reference">AVI RIFF File Reference</a>



<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>