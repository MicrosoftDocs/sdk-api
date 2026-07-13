---
UID: NN:strmif.ICaptureGraphBuilder
title: ICaptureGraphBuilder (strmif.h)
description: Note  This interface has been deprecated. (ICaptureGraphBuilder)
helpviewer_keywords: ["ICaptureGraphBuilder","ICaptureGraphBuilder interface [DirectShow]","ICaptureGraphBuilder interface [DirectShow]","described","ICaptureGraphBuilderInterface","dshow.icapturegraphbuilder","strmif/ICaptureGraphBuilder"]
old-location: dshow\icapturegraphbuilder.htm
tech.root: dshow
ms.assetid: 64ee80cd-9f63-4f38-853a-1ecfc03e6076
ms.date: 4/26/2023
ms.keywords: ICaptureGraphBuilder, ICaptureGraphBuilder interface [DirectShow], ICaptureGraphBuilder interface [DirectShow],described, ICaptureGraphBuilderInterface, dshow.icapturegraphbuilder, strmif/ICaptureGraphBuilder
req.header: strmif.h
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
 - ICaptureGraphBuilder
 - strmif/ICaptureGraphBuilder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - ICaptureGraphBuilder
---

# ICaptureGraphBuilder interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface has been deprecated. It will continue to be supported for backward compatibility with existing applications, but new applications should use the <a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2</a> interface.</div>
<div> </div>
The <code>ICaptureGraphBuilder</code> interface enables you to build capture graphs, preview graphs, file recompression graphs, or other custom graphs.

## -inheritance

The <b>ICaptureGraphBuilder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICaptureGraphBuilder</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
