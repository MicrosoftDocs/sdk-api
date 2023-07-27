---
UID: NN:strmif.IFilterGraph2
title: IFilterGraph2 (strmif.h)
description: The IFilterGraph2 interface extends the IFilterGraph and IGraphBuilder interfaces, which contain methods for building filter graphs.The Filter Graph Manager implements this interface.
helpviewer_keywords: ["IFilterGraph2","IFilterGraph2 interface [DirectShow]","IFilterGraph2 interface [DirectShow]","described","IFilterGraph2Interface","dshow.ifiltergraph2","strmif/IFilterGraph2"]
old-location: dshow\ifiltergraph2.htm
tech.root: dshow
ms.assetid: 1a1ef4fe-a054-4ba7-99c7-1f209472c5a6
ms.date: 4/26/2023
ms.keywords: IFilterGraph2, IFilterGraph2 interface [DirectShow], IFilterGraph2 interface [DirectShow],described, IFilterGraph2Interface, dshow.ifiltergraph2, strmif/IFilterGraph2
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IFilterGraph2
 - strmif/IFilterGraph2
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
 - IFilterGraph2
---

# IFilterGraph2 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IFilterGraph2</code> interface extends the <a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a> and <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interfaces, which contain methods for building filter graphs.

The Filter Graph Manager implements this interface. Applications can use it when building graphs, to take advantage of the additional methods it provides.

## -inheritance

The <b>IFilterGraph2</b> interface inherits from <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a>. <b>IFilterGraph2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a>
