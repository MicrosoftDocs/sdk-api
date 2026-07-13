---
UID: NS:aviriff._avistdindex
title: AVISTDINDEX (aviriff.h)
description: Contains an AVI 2.0 standard index.
helpviewer_keywords: ["AVISTDINDEX","AVISTDINDEX structure [DirectShow]","PAVISTDINDEX","PAVISTDINDEX structure pointer [DirectShow]","aviriff/AVISTDINDEX","aviriff/PAVISTDINDEX","dshow.avistdindex"]
old-location: dshow\avistdindex.htm
tech.root: DirectShow
ms.assetid: b437b333-84a3-44d3-a4cc-0d07a331b010
ms.date: 4/26/2023
ms.keywords: AVISTDINDEX, AVISTDINDEX structure [DirectShow], PAVISTDINDEX, PAVISTDINDEX structure pointer [DirectShow], aviriff/AVISTDINDEX, aviriff/PAVISTDINDEX, dshow.avistdindex
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
req.typenames: AVISTDINDEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _avistdindex
 - aviriff/_avistdindex
 - AVISTDINDEX
 - aviriff/AVISTDINDEX
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
 - AVISTDINDEX
---

# AVISTDINDEX structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Contains an AVI 2.0 standard index.

## -struct-fields

### -field fcc

A <b>FOURCC</b> code. The value is either  'indx' or '<i>nn</i>ix', where <i>nn</i> is the stream number.

### -field cb

The size of the structure, not including the initial 8 bytes.

### -field wLongsPerEntry

The size of each index entry, in 4-byte units. The value must be 2.

### -field bIndexSubType

The index subtype. The value must be zero.

### -field bIndexType

The index type. The value must be <b>AVI_INDEX_OF_CHUNKS</b>.

### -field nEntriesInUse

The number of valid entries in the <b>adwIndex</b> array.

### -field dwChunkId

A <b>FOURCC</b> that identifies the object that is indexed. This member has the same meaning as the <b>dwChunkId</b>  member of the <a href="/previous-versions/ms779634(v=vs.85)">AVIOLDINDEX</a> structure.

### -field qwBaseOffset

The base offset for the index entries. For each index entry, <b>qwBaseOffset</b> + <b>AVISTDINDEX_ENTRY.dwOffset</b> gives the offset from the start of the file to the data.

### -field dwReserved_3

Reserved. Set to zero.

### -field aIndex

An array of <a href="/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avistdindex_entry">AVISTDINDEX_ENTRY</a> structures. The number of elements in the array is calculated from the value of <b>cb</b>.

## -remarks

For more information, see the <i>OpenDML AVI File Format Extensions</i>, published by the OpenDML AVI M-JPEG File Format Subcommittee. (This resource may not be available in some languages 

and countries.)

## -see-also

<a href="/windows/desktop/DirectShow/avi-riff-file-reference">AVI RIFF File Reference</a>



<a href="/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex">AVIMETAINDEX</a>



<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>