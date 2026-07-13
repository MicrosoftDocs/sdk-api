---
UID: NF:austream.IMemoryData.SetBuffer
title: IMemoryData::SetBuffer (austream.h)
description: Note  This interface is deprecated. New applications should not use it. Initializes a memory buffer with a pointer to memory and length.
helpviewer_keywords: ["IMemoryData interface [DirectShow]","SetBuffer method","IMemoryData.SetBuffer","IMemoryData::SetBuffer","IMemoryDataSetBuffer","SetBuffer","SetBuffer method [DirectShow]","SetBuffer method [DirectShow]","IMemoryData interface","austream/IMemoryData::SetBuffer","dshow.imemorydata_setbuffer"]
old-location: dshow\imemorydata_setbuffer.htm
tech.root: dshow
ms.assetid: d565b493-0ee6-4a10-9af3-ff9d9ba48ba8
ms.date: 4/26/2023
ms.keywords: IMemoryData interface [DirectShow],SetBuffer method, IMemoryData.SetBuffer, IMemoryData::SetBuffer, IMemoryDataSetBuffer, SetBuffer, SetBuffer method [DirectShow], SetBuffer method [DirectShow],IMemoryData interface, austream/IMemoryData::SetBuffer, dshow.imemorydata_setbuffer
req.header: austream.h
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
 - IMemoryData::SetBuffer
 - austream/IMemoryData::SetBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - austream.h
api_name:
 - IMemoryData.SetBuffer
---

# IMemoryData::SetBuffer


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Initializes a memory buffer with a pointer to memory and length.

## -parameters

### -param cbSize [in]

Size of memory pointed to by <i>pbData</i>, in bytes.

### -param pbData [in]

Pointer to memory that this object will use.

### -param dwFlags [in]

Reserved for flag data. Must be zero.

## -returns

Returns S_OK if successful or E_INVALIDARG if <i>cbSize</i> is zero or <i>pbData</i> is <b>NULL</b>.

## -remarks

This method can be called as often as needed. When using <a href="/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update">IStreamSample::Update</a> to update samples asynchronously, make sure that SetBuffer is never called before an update is completed.

## -see-also

<a href="/windows/desktop/api/austream/nn-austream-imemorydata">IMemoryData Interface</a>