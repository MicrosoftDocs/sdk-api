---
UID: NN:strmif.IConfigAviMux
title: IConfigAviMux (strmif.h)
description: The IConfigAviMux interface configures the AVI Mux filter.
helpviewer_keywords: ["IConfigAviMux","IConfigAviMux interface [DirectShow]","IConfigAviMux interface [DirectShow]","described","IConfigAviMuxInterface","dshow.iconfigavimux","strmif/IConfigAviMux"]
old-location: dshow\iconfigavimux.htm
tech.root: dshow
ms.assetid: 4cc3cdeb-ebc5-46e1-8cc4-84b40e91323b
ms.date: 4/26/2023
ms.keywords: IConfigAviMux, IConfigAviMux interface [DirectShow], IConfigAviMux interface [DirectShow],described, IConfigAviMuxInterface, dshow.iconfigavimux, strmif/IConfigAviMux
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
 - IConfigAviMux
 - strmif/IConfigAviMux
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
 - IConfigAviMux
---

# IConfigAviMux interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IConfigAviMux</code> interface configures the <a href="/windows/desktop/DirectShow/avi-mux-filter">AVI Mux</a> filter. Applications can use this interface to set the master stream and to create an AVI 1.0 index.

[IConfigAviMux::GetOutputCompatibilityIndex](/windows/desktop/api/strmif/nf-strmif-iconfigavimux-getoutputcompatibilityindex) methods.

## -inheritance

The <b>IConfigAviMux</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConfigAviMux</b> also has these types of members:

