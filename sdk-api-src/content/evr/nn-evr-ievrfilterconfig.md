---
UID: NN:evr.IEVRFilterConfig
title: IEVRFilterConfig (evr.h)
description: Sets the number of input pins on the DirectShow Enhanced Video Renderer (EVR) filter.
helpviewer_keywords: ["13086d85-3dbf-4e9f-b065-d95e16412832","IEVRFilterConfig","IEVRFilterConfig interface [Media Foundation]","IEVRFilterConfig interface [Media Foundation]","described","evr/IEVRFilterConfig","mf.ievrfilterconfig"]
old-location: mf\ievrfilterconfig.htm
tech.root: mfarchive
ms.assetid: 13086d85-3dbf-4e9f-b065-d95e16412832
ms.date: 12/05/2018
ms.keywords: 13086d85-3dbf-4e9f-b065-d95e16412832, IEVRFilterConfig, IEVRFilterConfig interface [Media Foundation], IEVRFilterConfig interface [Media Foundation],described, evr/IEVRFilterConfig, mf.ievrfilterconfig
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IEVRFilterConfig
 - evr/IEVRFilterConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IEVRFilterConfig
archived: true
---

# IEVRFilterConfig interface


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Sets the number of input pins on the DirectShow <a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter">Enhanced Video Renderer</a> (EVR) filter. To get a pointer to this interface, call <b>QueryInterface</b> on the DirectShow EVR filter.

## -inheritance

The <b>IEVRFilterConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEVRFilterConfig</b> also has these types of members:

## -remarks

The DirectShow EVR filter starts with one input pin, which corresponds to the reference stream. To create additional pins for video substreams, call <a href="/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams">SetNumberOfStreams</a>.

The EVR media sink for Media Foundation does not support this interface. To add new streams to the EVR media sink, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink">IMFMediaSink::AddStreamSink</a>.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
