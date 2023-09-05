---
UID: NN:strmif.IPinConnection
title: IPinConnection (strmif.h)
description: This interface provides methods for reconnecting an input pin while the filter is still running.
helpviewer_keywords: ["IPinConnection","IPinConnection interface [DirectShow]","IPinConnection interface [DirectShow]","described","IPinConnectionInterface","dshow.ipinconnection","strmif/IPinConnection"]
old-location: dshow\ipinconnection.htm
tech.root: dshow
ms.assetid: 0843a01c-6f6a-4765-abca-dd562175fcee
ms.date: 4/26/2023
ms.keywords: IPinConnection, IPinConnection interface [DirectShow], IPinConnection interface [DirectShow],described, IPinConnectionInterface, dshow.ipinconnection, strmif/IPinConnection
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
 - IPinConnection
 - strmif/IPinConnection
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
 - IPinConnection
---

# IPinConnection interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

This interface provides methods for reconnecting an input pin while the filter is still running. The Filter Graph Manager calls methods on this interface when it performs dynamic reconnections (see the <a href="/windows/desktop/api/strmif/nn-strmif-igraphconfig">IGraphConfig</a> interface). Applications might also use this interface to perform dynamic pin reconnections.

<b>Filter developers: </b>Implement this interface on any input pin that allows dynamic reconnection or dynamic changes in format.

## -inheritance

The <b>IPinConnection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPinConnection</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/dynamic-graph-building">Dynamic Graph Building</a>



<a href="/windows/desktop/DirectShow/dynamic-reconnection">Dynamic Reconnection</a>
