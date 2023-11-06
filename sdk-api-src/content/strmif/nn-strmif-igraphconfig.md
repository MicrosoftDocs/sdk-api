---
UID: NN:strmif.IGraphConfig
title: IGraphConfig (strmif.h)
description: The Filter Graph Manager exposes IGraphConfig to support dynamic graph building.
helpviewer_keywords: ["IGraphConfig","IGraphConfig interface [DirectShow]","IGraphConfig interface [DirectShow]","described","IGraphConfigInterface","dshow.igraphconfig","strmif/IGraphConfig"]
old-location: dshow\igraphconfig.htm
tech.root: dshow
ms.assetid: 7df22157-9dd1-410e-b037-a155f7b9a01b
ms.date: 4/26/2023
ms.keywords: IGraphConfig, IGraphConfig interface [DirectShow], IGraphConfig interface [DirectShow],described, IGraphConfigInterface, dshow.igraphconfig, strmif/IGraphConfig
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
 - IGraphConfig
 - strmif/IGraphConfig
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
 - IGraphConfig
---

# IGraphConfig interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The Filter Graph Manager exposes <code>IGraphConfig</code> to support dynamic graph building. This interface enables applications and filters to reconfigure the filter graph while the graph is in a running state, and without losing data from the stream.

The most straightforward way to rebuild the graph dynamically is to call the <a href="/windows/desktop/api/strmif/nf-strmif-igraphconfig-reconnect">IGraphConfig::Reconnect</a> method. This method handles most of the details of dynamically rebuilding the graph. If a situation ever arises where you want to implement your own technique, <code>IGraphConfig</code> also provides the <a href="/windows/desktop/api/strmif/nf-strmif-igraphconfig-reconfigure">IGraphConfig::Reconfigure</a> method. This method obtains a lock on the filter graph and then calls a callback function in your application, which reconfigures the graph. With this method, most of the work is shifted to your application. For more information, see <a href="/windows/desktop/DirectShow/dynamic-graph-building">Dynamic Graph Building</a>.

To optimize the process of adding and removing filters, the filter graph maintains a cache of filters. During a call to the <b>Reconnect</b> method, you can specify that any filters removed from the graph get added to the cache. You can also add a filter to the cache directly, if you know it is likely to be needed, by calling <a href="/windows/desktop/api/strmif/nf-strmif-igraphconfig-addfiltertocache">IGraphConfig::AddFilterToCache</a>. The <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-render">IGraphBuilder::Render</a>, <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">IGraphBuilder::RenderFile</a>, and <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-connect">IGraphBuilder::Connect</a> methods automatically try to use filters in the cache before using other filters. Also, in the <b>Reconnect</b> method you can specify that only cached filters will be used for the reconnection. Note that filters held in the cache are not actually part of the graph. They are disconnected from any pins and are kept in a stopped state.

## -inheritance

The <b>IGraphConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGraphConfig</b> also has these types of members:

