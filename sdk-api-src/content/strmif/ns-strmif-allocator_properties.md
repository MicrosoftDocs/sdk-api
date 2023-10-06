---
UID: NS:strmif._AllocatorProperties
title: ALLOCATOR_PROPERTIES (strmif.h)
description: The ALLOCATOR_PROPERTIES structure describes an allocator's count, size, alignment, and prefix properties.
helpviewer_keywords: ["ALLOCATOR_PROPERTIES","ALLOCATOR_PROPERTIES structure [DirectShow]","ALLOCATOR_PROPERTIESStructure","dshow.allocator_properties","strmif/ALLOCATOR_PROPERTIES"]
old-location: dshow\allocator_properties.htm
tech.root: dshow
ms.assetid: 813e4693-b549-4045-aff5-08f2dd754b6e
ms.date: 4/26/2023
ms.keywords: ALLOCATOR_PROPERTIES, ALLOCATOR_PROPERTIES structure [DirectShow], ALLOCATOR_PROPERTIESStructure, dshow.allocator_properties, strmif/ALLOCATOR_PROPERTIES
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: ALLOCATOR_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AllocatorProperties
 - strmif/_AllocatorProperties
 - ALLOCATOR_PROPERTIES
 - strmif/ALLOCATOR_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - ALLOCATOR_PROPERTIES
---

# ALLOCATOR_PROPERTIES structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The ALLOCATOR_PROPERTIES structure describes an allocator's count, size, alignment, and prefix properties.

## -struct-fields

### -field cBuffers

Number of buffers created by the allocator.

### -field cbBuffer

Size of each buffer in bytes, excluding any prefix.

### -field cbAlign

Alignment of the buffer; buffer start will be aligned on a multiple of this value.

### -field cbPrefix

Each buffer is preceded by a prefix of this many bytes.

## -remarks

The <a href="/windows/desktop/api/strmif/nf-strmif-imediasample-getpointer">IMediaSample::GetPointer</a> method returns a pointer to the beginning of the buffer, not including the prefix bytes designated by <i>cbPrefix</i>.

The alignment is applied to the prefix data, if any. If a nonzero prefix is used, the beginning of the prefix is aligned according to <i>cbAlign</i>.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>