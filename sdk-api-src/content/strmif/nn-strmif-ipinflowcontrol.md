---
UID: NN:strmif.IPinFlowControl
title: IPinFlowControl (strmif.h)
description: Blocks data flow from an active output pin.
helpviewer_keywords: ["IPinFlowControl","IPinFlowControl interface [DirectShow]","IPinFlowControl interface [DirectShow]","described","IPinFlowControlInterface","dshow.ipinflowcontrol","strmif/IPinFlowControl"]
old-location: dshow\ipinflowcontrol.htm
tech.root: dshow
ms.assetid: 27e607d9-85f0-4e17-b8e7-6df729288acd
ms.date: 4/26/2023
ms.keywords: IPinFlowControl, IPinFlowControl interface [DirectShow], IPinFlowControl interface [DirectShow],described, IPinFlowControlInterface, dshow.ipinflowcontrol, strmif/IPinFlowControl
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
 - IPinFlowControl
 - strmif/IPinFlowControl
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
 - IPinFlowControl
---

# IPinFlowControl interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Blocks data flow from an active output pin. This interface is exposed by output pins that can reconnect dynamically. Use this interface to start a dynamic reconnection within the filter graph. For more information, see <a href="/windows/desktop/DirectShow/dynamic-graph-building">Dynamic Graph Building</a>.

<b>Filter developers: </b>Parser and capture filters that support dynamic reconnection should support this interface on their output pins. Generally, other types of filters do not need to implement this interface.

## -inheritance

The <b>IPinFlowControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPinFlowControl</b> also has these types of members:

