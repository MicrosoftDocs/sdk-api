---
UID: NN:strmif.IPin
title: IPin (strmif.h)
description: This interface is exposed by all input and output pins.The filter graph manager uses this interface to connect pins and perform flushing operations.
helpviewer_keywords: ["IPin","IPin interface [DirectShow]","IPin interface [DirectShow]","described","IPinInterface","dshow.ipin","strmif/IPin"]
old-location: dshow\ipin.htm
tech.root: dshow
ms.assetid: ad0ead4e-9f8e-4935-b220-306d665e50f4
ms.date: 4/26/2023
ms.keywords: IPin, IPin interface [DirectShow], IPin interface [DirectShow],described, IPinInterface, dshow.ipin, strmif/IPin
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
 - IPin
 - strmif/IPin
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
 - IPin
---

# IPin interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

This interface is exposed by all input and output pins.

The filter graph manager uses this interface to connect pins and perform flushing operations. Applications can use this interface to query the pin for information. Applications should never call <code>IPin</code> methods that change a pin's state, such as <a href="/windows/desktop/api/strmif/nf-strmif-ipin-connect">Connect</a>, <a href="/windows/desktop/api/strmif/nf-strmif-ipin-disconnect">Disconnect</a>, <a href="/windows/desktop/api/strmif/nf-strmif-ipin-beginflush">BeginFlush</a>, or <a href="/windows/desktop/api/strmif/nf-strmif-ipin-endflush">EndFlush</a>. To connect pins, an application must use the methods in <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a>.

<b>Filter developers: </b>The <a href="/windows/desktop/DirectShow/cbasepin">CBasePin</a>, <a href="/windows/desktop/DirectShow/cbaseinputpin">CBaseInputPin</a>, and <a href="/windows/desktop/DirectShow/cbaseoutputpin">CBaseOutputPin</a> classes implement this interface. Other base classes derive from these three classes.

## -inheritance

The <b>IPin</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPin</b> also has these types of members:

