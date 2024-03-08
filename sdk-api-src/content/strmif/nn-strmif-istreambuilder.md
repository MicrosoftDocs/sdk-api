---
UID: NN:strmif.IStreamBuilder
title: IStreamBuilder (strmif.h)
description: The IStreamBuilder interface enables an output pin to notify the filter graph manager that the pin itself will build the downstream section of the filter graph.
helpviewer_keywords: ["IStreamBuilder","IStreamBuilder interface [DirectShow]","IStreamBuilder interface [DirectShow]","described","IStreamBuilderInterface","dshow.istreambuilder","strmif/IStreamBuilder"]
old-location: dshow\istreambuilder.htm
tech.root: dshow
ms.assetid: 233821e9-9916-4047-a554-4ff43769819f
ms.date: 4/26/2023
ms.keywords: IStreamBuilder, IStreamBuilder interface [DirectShow], IStreamBuilder interface [DirectShow],described, IStreamBuilderInterface, dshow.istreambuilder, strmif/IStreamBuilder
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
 - IStreamBuilder
 - strmif/IStreamBuilder
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
 - IStreamBuilder
---

# IStreamBuilder interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IStreamBuilder</code> interface enables an output pin to notify the filter graph manager that the pin itself will build the downstream section of the filter graph. Output pins with special connection needs can implement this interface to override the default pin connection process used by the filter graph manager.

## -inheritance

The <b>IStreamBuilder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamBuilder</b> also has these types of members:

