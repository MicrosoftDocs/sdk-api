---
UID: NN:austream.IMemoryData
title: IMemoryData (austream.h)
description: Note  This interface is deprecated.
helpviewer_keywords: ["IMemoryData","IMemoryData interface [DirectShow]","IMemoryData interface [DirectShow]","described","IMemoryDataInterface","austream/IMemoryData","dshow.imemorydata"]
old-location: dshow\imemorydata.htm
tech.root: dshow
ms.assetid: 0e809ae7-381c-4ada-8940-5d42bf5c03da
ms.date: 4/26/2023
ms.keywords: IMemoryData, IMemoryData interface [DirectShow], IMemoryData interface [DirectShow],described, IMemoryDataInterface, austream/IMemoryData, dshow.imemorydata
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
 - IMemoryData
 - austream/IMemoryData
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
 - IMemoryData
---

# IMemoryData interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IMemoryData</code> interface contains methods that set and retrieve memory data on audio data objects. Audio data objects provide the underlying data which stream samples access. This interface provides a way to initialize memory buffers and to set actual amounts of audio data in the objects. Additionally, the <a href="/windows/desktop/api/austream/nf-austream-imemorydata-getinfo">GetInfo</a> method can be used to retrieve audio memory data.

Implement this interface on underlying audio data objects that audio stream sample objects will access.

Typically these methods are called by the <a href="/windows/desktop/api/austream/nn-austream-iaudiomediastream">IAudioMediaStream</a> or <a href="/windows/desktop/api/austream/nn-austream-iaudiostreamsample">IAudioStreamSample</a> object, rather than by the application.

In addition to the methods inherited from <b>IUnknown</b>, the <code>IMemoryData</code> interface exposes the following methods.

## -inheritance

The <b>IMemoryData</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMemoryData</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

