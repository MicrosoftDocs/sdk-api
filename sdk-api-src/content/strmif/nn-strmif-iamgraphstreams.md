---
UID: NN:strmif.IAMGraphStreams
title: IAMGraphStreams (strmif.h)
description: The IAMGraphStreams interface controls a filter graph that renders a live source.
helpviewer_keywords: ["IAMGraphStreams","IAMGraphStreams interface [DirectShow]","IAMGraphStreams interface [DirectShow]","described","IAMGraphStreamsInterface","dshow.iamgraphstreams","strmif/IAMGraphStreams"]
old-location: dshow\iamgraphstreams.htm
tech.root: dshow
ms.assetid: 30d44536-2a2d-44ab-bafc-bdb851cd272b
ms.date: 12/05/2018
ms.keywords: IAMGraphStreams, IAMGraphStreams interface [DirectShow], IAMGraphStreams interface [DirectShow],described, IAMGraphStreamsInterface, dshow.iamgraphstreams, strmif/IAMGraphStreams
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
 - IAMGraphStreams
 - strmif/IAMGraphStreams
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
 - IAMGraphStreams
---

# IAMGraphStreams interface


## -description

The <code>IAMGraphStreams</code> interface controls a filter graph that renders a live source. A live source is one that streams data in real time, such as a capture device or a network broadcast. The Filter Graph Manager implements this interface.

Applications can use this interface to specify how the graph handles latency and synchronization when it renders a live source. For more information, see <a href="/windows/desktop/DirectShow/live-sources">Live Sources</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMGraphStreams</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMGraphStreams</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

