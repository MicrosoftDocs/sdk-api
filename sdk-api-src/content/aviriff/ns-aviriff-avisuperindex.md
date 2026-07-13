---
UID: NS:aviriff._avisuperindex
title: AVISUPERINDEX (aviriff.h)
description: Contains an AVI 2.0 super index (index of indexes).
helpviewer_keywords: ["AVISUPERINDEX","AVISUPERINDEX structure [DirectShow]","aviriff/AVISUPERINDEX","dshow.avisuperindex"]
old-location: dshow\avisuperindex.htm
tech.root: DirectShow
ms.assetid: 57c855ef-d4ea-4e11-a37b-941335ccf657
ms.date: 4/26/2023
ms.keywords: AVISUPERINDEX, AVISUPERINDEX structure [DirectShow], aviriff/AVISUPERINDEX, dshow.avisuperindex
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
req.typenames: AVISUPERINDEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _avisuperindex
 - aviriff/_avisuperindex
 - AVISUPERINDEX
 - aviriff/AVISUPERINDEX
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
 - AVISUPERINDEX
---

# AVISUPERINDEX structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Contains an AVI 2.0 super index (index of indexes).

## -struct-fields

### -field fcc

A <b>FOURCC</b> code. The value must be 'indx'.

### -field cb

The size of the structure, not including the initial 8 bytes.

### -field wLongsPerEntry

The size of each index entry, in 4-byte units. The value must be 4.

### -field bIndexSubType

The index subtype. The value must be zero or <b>AVI_INDEX_SUB_2FIELD</b>.

### -field bIndexType

The index type. The value must be <b>AVI_INDEX_OF_INDEXES</b>.

### -field nEntriesInUse

The number of valid entries in the <b>adwIndex</b> array.

### -field dwChunkId

A <b>FOURCC</b> that identifies the object that is indexed.

### -field dwReserved

Reserved. Set the array elements to zero.

### -field _avisuperindex_entry

### -field _avisuperindex_entry.qwOffset

### -field _avisuperindex_entry.dwSize

### -field _avisuperindex_entry.dwDuration

### -field aIndex

An array of structures that contain the following members. The number of elements in the array is calculated from the value of <b>cb</b>.



#### qwOffset

The offset, in bytes, from the start of the file to the sub-index that this entry points to.



#### dwSize

The size of the sub-index, in bytes.



#### dwDuration

The duration of the file that is covered by the sub-index, in stream ticks.

## -remarks

For more information, see the <i>OpenDML AVI File Format Extensions</i>, published by the OpenDML AVI M-JPEG File Format Subcommittee. (This resource may not be available in some languages 

and countries.)

## -see-also

<a href="/windows/desktop/DirectShow/avi-riff-file-reference">AVI RIFF File Reference</a>



<a href="/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex">AVIMETAINDEX</a>



<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>