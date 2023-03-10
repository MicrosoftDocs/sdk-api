---
UID: NN:strmif.IPersistMediaPropertyBag
title: IPersistMediaPropertyBag (strmif.h)
description: The IPersistMediaPropertyBag interface sets and retrieves INFO and DISP chunks in Audio-Video Interleaved (AVI) streams.
helpviewer_keywords: ["IPersistMediaPropertyBag","IPersistMediaPropertyBag interface [DirectShow]","IPersistMediaPropertyBag interface [DirectShow]","described","IPersistMediaPropertyBagInterface","dshow.ipersistmediapropertybag","strmif/IPersistMediaPropertyBag"]
old-location: dshow\ipersistmediapropertybag.htm
tech.root: dshow
ms.assetid: 33e4b76b-841a-4dc5-b117-e08a6f4dcbe7
ms.date: 12/05/2018
ms.keywords: IPersistMediaPropertyBag, IPersistMediaPropertyBag interface [DirectShow], IPersistMediaPropertyBag interface [DirectShow],described, IPersistMediaPropertyBagInterface, dshow.ipersistmediapropertybag, strmif/IPersistMediaPropertyBag
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
 - IPersistMediaPropertyBag
 - strmif/IPersistMediaPropertyBag
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
 - IPersistMediaPropertyBag
---

# IPersistMediaPropertyBag interface


## -description

The <code>IPersistMediaPropertyBag</code> interface sets and retrieves INFO and DISP chunks in Audio-Video Interleaved (AVI) streams. It uses the <a href="/windows/desktop/api/strmif/nn-strmif-imediapropertybag">IMediaPropertyBag</a> interface to store the chunks as name/value pairs.

The <a href="/windows/desktop/DirectShow/avi-splitter-filter">AVI Splitter</a> filter and the <a href="/windows/desktop/DirectShow/wave-parser-filter">WAVE Parser</a> filter support this interface for reading INFO and DISP chunks from an AVI or WAV file. The <a href="/windows/desktop/DirectShow/avi-mux-filter">AVI Mux</a> filter supports the interface for writing these chunks into a file.

<code>IPersistMediaPropertyBag</code> is modeled after, but does not inherit from, the <b>IPersistPropertyBag</b> interface. For more information on <b>IPersistPropertyBag</b>, see the Platform SDK.

## -inheritance

The <b>IPersistMediaPropertyBag</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPersistMediaPropertyBag</b> also has these types of members:

