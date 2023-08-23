---
UID: NN:strmif.IDVSplitter
title: IDVSplitter (strmif.h)
description: Downgrades the frame rate on a digital video (DV) stream.
helpviewer_keywords: ["IDVSplitter","IDVSplitter interface [DirectShow]","IDVSplitter interface [DirectShow]","described","IDVSplitterInterface","dshow.idvsplitter","strmif/IDVSplitter"]
old-location: dshow\idvsplitter.htm
tech.root: dshow
ms.assetid: a7fd27f4-2fc7-4115-b669-b08eed1ec032
ms.date: 4/26/2023
ms.keywords: IDVSplitter, IDVSplitter interface [DirectShow], IDVSplitter interface [DirectShow],described, IDVSplitterInterface, dshow.idvsplitter, strmif/IDVSplitter
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDVSplitter
 - strmif/IDVSplitter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDVSplitter
---

# IDVSplitter interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Downgrades the frame rate on a digital video (DV) stream. The <a href="/windows/desktop/DirectShow/dv-splitter-filter">DV Splitter</a> filter exposes this interface.

Applications can use this interface to reduce the frame rate on a DV stream, before the stream reaches the <a href="/windows/desktop/DirectShow/dv-video-decoder-filter">DV Video Decoder</a> filter. This can be helpful for processor-intensive tasks, such as real-time transcoding.

## -inheritance

The <b>IDVSplitter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVSplitter</b> also has these types of members:

