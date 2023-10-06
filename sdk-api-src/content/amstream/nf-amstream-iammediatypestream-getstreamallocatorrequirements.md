---
UID: NF:amstream.IAMMediaTypeStream.GetStreamAllocatorRequirements
title: IAMMediaTypeStream::GetStreamAllocatorRequirements (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetStreamAllocatorRequirements retrieves the allocator requirements for the stream. This method is not currently implemented.
helpviewer_keywords: ["GetStreamAllocatorRequirements","GetStreamAllocatorRequirements method [DirectShow]","GetStreamAllocatorRequirements method [DirectShow]","IAMMediaTypeStream interface","IAMMediaTypeStream interface [DirectShow]","GetStreamAllocatorRequirements method","IAMMediaTypeStream.GetStreamAllocatorRequirements","IAMMediaTypeStream::GetStreamAllocatorRequirements","IAMMediaTypeStreamGetStreamAllocatorRequirements","amstream/IAMMediaTypeStream::GetStreamAllocatorRequirements","dshow.iammediatypestream_getstreamallocatorrequirements"]
old-location: dshow\iammediatypestream_getstreamallocatorrequirements.htm
tech.root: dshow
ms.assetid: 0a1ad5c5-0cbf-44a5-833f-951c9934bd19
ms.date: 4/26/2023
ms.keywords: GetStreamAllocatorRequirements, GetStreamAllocatorRequirements method [DirectShow], GetStreamAllocatorRequirements method [DirectShow],IAMMediaTypeStream interface, IAMMediaTypeStream interface [DirectShow],GetStreamAllocatorRequirements method, IAMMediaTypeStream.GetStreamAllocatorRequirements, IAMMediaTypeStream::GetStreamAllocatorRequirements, IAMMediaTypeStreamGetStreamAllocatorRequirements, amstream/IAMMediaTypeStream::GetStreamAllocatorRequirements, dshow.iammediatypestream_getstreamallocatorrequirements
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
 - IAMMediaTypeStream::GetStreamAllocatorRequirements
 - amstream/IAMMediaTypeStream::GetStreamAllocatorRequirements
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
 - IAMMediaTypeStream.GetStreamAllocatorRequirements
---

# IAMMediaTypeStream::GetStreamAllocatorRequirements


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetStreamAllocatorRequirements</code> retrieves the allocator requirements for the stream. This method is not currently implemented.

## -parameters

### -param pProps [out]

Pointer to an <a href="/windows/win32/api/strmif/ns-strmif-allocator_properties">ALLOCATOR_PROPERTIES</a> structure that receives the stream allocator requirements.

## -returns

Returns E_FAIL.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypestream">IAMMediaTypeStream Interface</a>