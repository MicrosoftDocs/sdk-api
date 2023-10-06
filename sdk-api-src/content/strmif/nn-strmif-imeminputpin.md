---
UID: NN:strmif.IMemInputPin
title: IMemInputPin (strmif.h)
description: The IMemInputPin interface delivers media data to an input pin.
helpviewer_keywords: ["IMemInputPin","IMemInputPin interface [DirectShow]","IMemInputPin interface [DirectShow]","described","IMemInputPinInterface","dshow.imeminputpin","strmif/IMemInputPin"]
old-location: dshow\imeminputpin.htm
tech.root: dshow
ms.assetid: a4407c6f-6bb5-4274-920b-8bf7d76268bc
ms.date: 4/26/2023
ms.keywords: IMemInputPin, IMemInputPin interface [DirectShow], IMemInputPin interface [DirectShow],described, IMemInputPinInterface, dshow.imeminputpin, strmif/IMemInputPin
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
 - IMemInputPin
 - strmif/IMemInputPin
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
 - IMemInputPin
---

# IMemInputPin interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IMemInputPin</code> interface delivers media data to an input pin. Input pins expose this interface if they use the <a href="/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator</a> interface to allocate buffers. When an output pin connects to an input pin, the output pin uses this interface to negotiate allocator requirements and deliver samples to the input pin.

Applications typically do not use this interface.

<b>Filter developers: </b>The <a href="/windows/desktop/DirectShow/cbaseinputpin">CBaseInputPin</a> class implements this interface.

## -inheritance

The <b>IMemInputPin</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMemInputPin</b> also has these types of members:

