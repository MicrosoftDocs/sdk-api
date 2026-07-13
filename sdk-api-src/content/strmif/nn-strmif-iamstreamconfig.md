---
UID: NN:strmif.IAMStreamConfig
title: IAMStreamConfig (strmif.h)
description: The IAMStreamConfig interface sets the output format on certain capture and compression filters, for both audio and video.
helpviewer_keywords: ["IAMStreamConfig","IAMStreamConfig interface [DirectShow]","IAMStreamConfig interface [DirectShow]","described","IAMStreamConfigInterface","dshow.iamstreamconfig","strmif/IAMStreamConfig"]
old-location: dshow\iamstreamconfig.htm
tech.root: dshow
ms.assetid: c171763e-9108-49a0-a4b7-855c6db0a71d
ms.date: 4/26/2023
ms.keywords: IAMStreamConfig, IAMStreamConfig interface [DirectShow], IAMStreamConfig interface [DirectShow],described, IAMStreamConfigInterface, dshow.iamstreamconfig, strmif/IAMStreamConfig
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
 - IAMStreamConfig
 - strmif/IAMStreamConfig
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
 - IAMStreamConfig
---

# IAMStreamConfig interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IAMStreamConfig</b> interface sets the output format on certain capture and compression filters, for both audio and video. Applications can use this interface to set format properties, such as the output dimensions and frame rate (for video) or the sample rate and number of channels (for audio).

## -inheritance

The <b>IAMStreamConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMStreamConfig</b> also has these types of members:

## -remarks

Filters expose this interface on their output pins. To use the interface, enumerate the filter's pins and query for <b>IAMStreamConfig</b>. Or, if you are using the <a href="/windows/desktop/DirectShow/capture-graph-builder">Capture Graph Builder</a> object to build the filter graph, you can call the <a href="/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-findinterface">ICaptureGraphBuilder2::FindInterface</a> method. Note that a capture filter might have separate pins for capture and preview.

<h3><a id="Filter_Developers"></a><a id="filter_developers"></a><a id="FILTER_DEVELOPERS"></a>Filter Developers</h3>
If you are writing a capture filter or compression filter, implement this interface on the video or audio output pin. For more information, see <a href="/windows/desktop/DirectShow/exposing-capture-and-compression-formats">Exposing Capture and Compression Formats</a>.

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
