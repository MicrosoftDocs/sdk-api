---
UID: NS:aviriff._avimetaindex
title: AVIMETAINDEX (aviriff.h)
description: The base structure for an AVI 2.0 index ('indx' format).
helpviewer_keywords: ["AVIMETAINDEX","AVIMETAINDEX structure [DirectShow]","AVI_INDEX_IS_DATA","AVI_INDEX_OF_CHUNKS","AVI_INDEX_OF_INDEXES","aviriff/AVIMETAINDEX","dshow.avimetaindex"]
old-location: dshow\avimetaindex.htm
tech.root: DirectShow
ms.assetid: d27b2b14-55a1-4992-ad85-75244369accc
ms.date: 4/26/2023
ms.keywords: AVIMETAINDEX, AVIMETAINDEX structure [DirectShow], AVI_INDEX_IS_DATA, AVI_INDEX_OF_CHUNKS, AVI_INDEX_OF_INDEXES, aviriff/AVIMETAINDEX, dshow.avimetaindex
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
req.typenames: AVIMETAINDEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _avimetaindex
 - aviriff/_avimetaindex
 - AVIMETAINDEX
 - aviriff/AVIMETAINDEX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - aviriff.h
api_name:
 - AVIMETAINDEX
---

# AVIMETAINDEX structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The base structure for an AVI 2.0 index ('indx' format).

## -struct-fields

### -field fcc

A <b>FOURCC</b> code. The value is either 'indx' or '<i>nn</i>ix', where <i>nn</i> is the stream number.

### -field cb

The size of the structure, not including the initial 8 bytes.

### -field wLongsPerEntry

The size of each index entry, in 4-byte units.

### -field bIndexSubType

The index subtype. The meaning depends on the value of <b>bIndexType</b>.

### -field bIndexType

The index type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AVI_INDEX_OF_INDEXES"></a><a id="avi_index_of_indexes"></a><dl>
<dt><b>AVI_INDEX_OF_INDEXES</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
Each index entry points to another index. Treat the <b>AVIMETAINDEX</b> structure as an <a href="/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avisuperindex">AVISUPERINDEX</a> structure. The value of <b>bIndexSubType</b> must be zero.

</td>
</tr>
<tr>
<td width="40%"><a id="AVI_INDEX_OF_CHUNKS"></a><a id="avi_index_of_chunks"></a><dl>
<dt><b>AVI_INDEX_OF_CHUNKS</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Each index entry points to a data chunk in the file. 

<ul>
<li>If <b>bIndexSubType</b> is 0,  treat the <b>AVIMETAINDEX</b> structure as an <a href="/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avistdindex">AVISTDINDEX</a> structure. Each index entry is an <a href="/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avistdindex_entry">AVISTDINDEX_ENTRY</a> structure.</li>
<li>If <b>bIndexSubType</b> is <b>AVI_INDEX_SUB_2FIELD</b>, the index is a field index chunk.<div class="alert"><b>Note</b>  DirectShow does not support field indexes.</div>
<div> </div>
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="AVI_INDEX_IS_DATA"></a><a id="avi_index_is_data"></a><dl>
<dt><b>AVI_INDEX_IS_DATA</b></dt>
<dt>0x80</dt>
</dl>
</td>
<td width="60%">
The <b>adwIndex</b> array contains a table of data, not a list of index entries.

</td>
</tr>
</table>

### -field nEntriesInUse

The number of valid entries in the <b>adwIndex</b> array.

### -field dwChunkId

A <b>FOURCC</b> that identifies the object that is indexed. If the indexed object is a stream, this member has the same meaning as the <b>dwChunkId</b>  member of the <a href="/previous-versions/ms779634(v=vs.85)">AVIOLDINDEX</a> structure.

### -field dwReserved

The meaning of this member depends on the index type.

### -field adwIndex

An array of index entries. The format of this data depends on the index type.

## -remarks

For more information, see the <i>OpenDML AVI File Format Extensions</i>, published by the OpenDML AVI M-JPEG File Format Subcommittee. (This resource may not be available in some languages 

and countries.)

## -see-also

<a href="/windows/desktop/DirectShow/avi-riff-file-reference">AVI RIFF File Reference</a>



<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>