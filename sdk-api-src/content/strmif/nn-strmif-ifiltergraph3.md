---
UID: NN:strmif.IFilterGraph3
title: IFilterGraph3 (strmif.h)
description: The IFilterGraph3 interface extends the IFilterGraph2 interface, which contains methods for building filter graphs.The Filter Graph Manager implements this interface.
helpviewer_keywords: ["IFilterGraph3","IFilterGraph3 interface [DirectShow]","IFilterGraph3 interface [DirectShow]","described","IFilterGraph3Interface","dshow.ifiltergraph3","strmif/IFilterGraph3"]
old-location: dshow\ifiltergraph3.htm
tech.root: dshow
ms.assetid: 1d5f8eda-2b09-4627-8ae9-f43f38c3c26a
ms.date: 4/26/2023
ms.keywords: IFilterGraph3, IFilterGraph3 interface [DirectShow], IFilterGraph3 interface [DirectShow],described, IFilterGraph3Interface, dshow.ifiltergraph3, strmif/IFilterGraph3
req.header: strmif.h
req.include-header: Dshow.h
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
 - IFilterGraph3
 - strmif/IFilterGraph3
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
 - IFilterGraph3
---

# IFilterGraph3 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IFilterGraph3</code> interface extends the <a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph2">IFilterGraph2</a> interface, which contains methods for building filter graphs.

The Filter Graph Manager implements this interface. Applications can use it when building graphs, to take advantage of the additional methods it provides.

## -inheritance

The <b>IFilterGraph3</b> interface inherits from <b>IFilterGraph2</b>. <b>IFilterGraph3</b> also has these types of members:

