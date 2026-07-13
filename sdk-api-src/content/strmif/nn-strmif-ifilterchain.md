---
UID: NN:strmif.IFilterChain
title: IFilterChain (strmif.h)
description: The IFilterChain interface provides methods for starting, stopping, or removing chains of filters in a filter graph.
helpviewer_keywords: ["IFilterChain","IFilterChain interface [DirectShow]","IFilterChain interface [DirectShow]","described","IFilterChainInterface","dshow.ifilterchain","strmif/IFilterChain"]
old-location: dshow\ifilterchain.htm
tech.root: dshow
ms.assetid: 04fa1e89-19cd-488e-9df2-8a5fd2c3f445
ms.date: 4/26/2023
ms.keywords: IFilterChain, IFilterChain interface [DirectShow], IFilterChain interface [DirectShow],described, IFilterChainInterface, dshow.ifilterchain, strmif/IFilterChain
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
 - IFilterChain
 - strmif/IFilterChain
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
 - IFilterChain
---

# IFilterChain interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IFilterChain</code> interface provides methods for starting, stopping, or removing chains of filters in a filter graph. The filter graph manager exposes this interface.

A <i>filter chain</i> is a sequence of filters, each with at most one connected input pin and one connected output pin, that forms an unbroken line of filters. A filter chain is defined by the filter at the start of the chain and the filter at the end of the chain. (These can be the same filter, making a chain of one filter.) By definition, there is a single stream path going from the start of the chain downstream to the end of the chain.

The methods on this interface are useful in situations where an entire stream of data can appear or disappear, such as a video conferencing application that receives multiple streams over a network. For more information, see <a href="/windows/desktop/DirectShow/dynamic-graph-building">Dynamic Graph Building</a>. To control individual streams on a capture filter, use the <a href="/windows/desktop/api/strmif/nn-strmif-iamstreamcontrol">IAMStreamControl</a> interface instead.

## -inheritance

The <b>IFilterChain</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFilterChain</b> also has these types of members:

