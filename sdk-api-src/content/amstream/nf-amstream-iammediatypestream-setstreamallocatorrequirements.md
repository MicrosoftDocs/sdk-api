---
UID: NF:amstream.IAMMediaTypeStream.SetStreamAllocatorRequirements
title: IAMMediaTypeStream::SetStreamAllocatorRequirements (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The SetStreamAllocatorRequirements sets the allocator requirements for the stream. This method is not currently implemented.
helpviewer_keywords: ["IAMMediaTypeStream interface [DirectShow]","SetStreamAllocatorRequirements method","IAMMediaTypeStream.SetStreamAllocatorRequirements","IAMMediaTypeStream::SetStreamAllocatorRequirements","IAMMediaTypeStreamSetStreamAllocatorRequirements","SetStreamAllocatorRequirements","SetStreamAllocatorRequirements method [DirectShow]","SetStreamAllocatorRequirements method [DirectShow]","IAMMediaTypeStream interface","amstream/IAMMediaTypeStream::SetStreamAllocatorRequirements","dshow.iammediatypestream_setstreamallocatorrequirements"]
old-location: dshow\iammediatypestream_setstreamallocatorrequirements.htm
tech.root: dshow
ms.assetid: d34a00dd-e863-4356-97f9-da3776ecb47b
ms.date: 4/26/2023
ms.keywords: IAMMediaTypeStream interface [DirectShow],SetStreamAllocatorRequirements method, IAMMediaTypeStream.SetStreamAllocatorRequirements, IAMMediaTypeStream::SetStreamAllocatorRequirements, IAMMediaTypeStreamSetStreamAllocatorRequirements, SetStreamAllocatorRequirements, SetStreamAllocatorRequirements method [DirectShow], SetStreamAllocatorRequirements method [DirectShow],IAMMediaTypeStream interface, amstream/IAMMediaTypeStream::SetStreamAllocatorRequirements, dshow.iammediatypestream_setstreamallocatorrequirements
req.header: amstream.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMMediaTypeStream::SetStreamAllocatorRequirements
 - amstream/IAMMediaTypeStream::SetStreamAllocatorRequirements
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaTypeStream.SetStreamAllocatorRequirements
---

# IAMMediaTypeStream::SetStreamAllocatorRequirements


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetStreamAllocatorRequirements</code> sets the allocator requirements for the stream. This method is not currently implemented.

## -parameters

### -param pProps [in]

Pointer to an <a href="/windows/win32/api/strmif/ns-strmif-allocator_properties">ALLOCATOR_PROPERTIES</a> structure that contains the stream allocator requirements.

## -returns

Returns E_FAIL.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypestream">IAMMediaTypeStream Interface</a>