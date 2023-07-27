---
UID: NN:strmif.IGraphVersion
title: IGraphVersion (strmif.h)
description: The IGraphVersion interface is implemented on the Filter Graph Manager to provide a way for plug-in distributors and applications to know when the graph has changed.
helpviewer_keywords: ["IGraphVersion","IGraphVersion interface [DirectShow]","IGraphVersion interface [DirectShow]","described","IGraphVersionInterface","dshow.igraphversion","strmif/IGraphVersion"]
old-location: dshow\igraphversion.htm
tech.root: dshow
ms.assetid: abca59f2-2134-4938-9933-bacaed771d0d
ms.date: 4/26/2023
ms.keywords: IGraphVersion, IGraphVersion interface [DirectShow], IGraphVersion interface [DirectShow],described, IGraphVersionInterface, dshow.igraphversion, strmif/IGraphVersion
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
 - IGraphVersion
 - strmif/IGraphVersion
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
 - IGraphVersion
---

# IGraphVersion interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IGraphVersion</code> interface is implemented on the Filter Graph Manager to provide a way for plug-in distributors and applications to know when the graph has changed. If the graph has changed, and the application or plug-in distributor has an interface on a particular filter or pin, it should requery the graph to see if its pointers are still valid, or if there are new ones it should use.

## -inheritance

The <b>IGraphVersion</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGraphVersion</b> also has these types of members:

