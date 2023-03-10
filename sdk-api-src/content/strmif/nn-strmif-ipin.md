---
UID: NN:strmif.IPin
title: IPin (strmif.h)
description: This interface is exposed by all input and output pins.The filter graph manager uses this interface to connect pins and perform flushing operations.
helpviewer_keywords: ["IPin","IPin interface [DirectShow]","IPin interface [DirectShow]","described","IPinInterface","dshow.ipin","strmif/IPin"]
old-location: dshow\ipin.htm
tech.root: dshow
ms.assetid: ad0ead4e-9f8e-4935-b220-306d665e50f4
ms.date: 12/05/2018
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

This interface is exposed by all input and output pins.

The filter graph manager uses this interface to connect pins and perform flushing operations. Applications can use this interface to query the pin for information. Applications should never call <code>IPin</code> methods that change a pin's state, such as <a href="/windows/desktop/api/strmif/nf-strmif-ipin-connect">Connect</a>, <a href="/windows/desktop/api/strmif/nf-strmif-ipin-disconnect">Disconnect</a>, <a href="/windows/desktop/api/strmif/nf-strmif-ipin-beginflush">BeginFlush</a>, or <a href="/windows/desktop/api/strmif/nf-strmif-ipin-endflush">EndFlush</a>. To connect pins, an application must use the methods in <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a>.

<b>Filter developers: </b>The <a href="/windows/desktop/DirectShow/cbasepin">CBasePin</a>, <a href="/windows/desktop/DirectShow/cbaseinputpin">CBaseInputPin</a>, and <a href="/windows/desktop/DirectShow/cbaseoutputpin">CBaseOutputPin</a> classes implement this interface. Other base classes derive from these three classes.

## -inheritance

The <b>IPin</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPin</b> also has these types of members:

