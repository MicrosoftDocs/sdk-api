---
UID: NS:aviriff._avistdindex_entry
title: AVISTDINDEX_ENTRY (aviriff.h)
description: Contains one index entry for an AVI 2.0 standard index.
helpviewer_keywords: ["AVISTDINDEX_ENTRY","AVISTDINDEX_ENTRY structure [DirectShow]","aviriff/AVISTDINDEX_ENTRY","dshow.avistdindex_entry"]
old-location: dshow\avistdindex_entry.htm
tech.root: dshow
ms.assetid: 4e408858-b0cb-45dc-a299-a2e35aa6a000
ms.date: 4/26/2023
ms.keywords: AVISTDINDEX_ENTRY, AVISTDINDEX_ENTRY structure [DirectShow], aviriff/AVISTDINDEX_ENTRY, dshow.avistdindex_entry
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
req.typenames: AVISTDINDEX_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _avistdindex_entry
 - aviriff/_avistdindex_entry
 - AVISTDINDEX_ENTRY
 - aviriff/AVISTDINDEX_ENTRY
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
 - AVISTDINDEX_ENTRY
---

# AVISTDINDEX_ENTRY structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Contains one index entry for an AVI 2.0 standard index. This structure is contained in the <a href="/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avistdindex">AVISTDINDEX</a> structure.

## -struct-fields

### -field dwOffset

The offset, in bytes, to the start of the data. The offset is relative to the value of the <b>qwBaseOffset</b> member of the <a href="/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avistdindex">AVISTDINDEX</a>. The value is the offset of the actual audio/video data in the chunk, not the offset of the start of the chunk.

### -field dwSize

The lower 31 bits contain the size of the data. The high bit is set to 1 if the frame is delta frame, or zero otherwise.

## -remarks

For more information, see the <i>OpenDML AVI File Format Extensions</i>, published by the OpenDML AVI M-JPEG File Format Subcommittee. (This resource may not be available in some languages 

and countries.)

## -see-also

<a href="/windows/desktop/DirectShow/avi-riff-file-reference">AVI RIFF File Reference</a>



<a href="/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avistdindex">AVISTDINDEX</a>



<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>