---
UID: NN:strmif.IMemInputPin
title: IMemInputPin (strmif.h)
description: The IMemInputPin interface delivers media data to an input pin.
helpviewer_keywords: ["IMemInputPin","IMemInputPin interface [DirectShow]","IMemInputPin interface [DirectShow]","described","IMemInputPinInterface","dshow.imeminputpin","strmif/IMemInputPin"]
old-location: dshow\imeminputpin.htm
tech.root: dshow
ms.assetid: a4407c6f-6bb5-4274-920b-8bf7d76268bc
ms.date: 12/05/2018
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

The <code>IMemInputPin</code> interface delivers media data to an input pin. Input pins expose this interface if they use the <a href="/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator</a> interface to allocate buffers. When an output pin connects to an input pin, the output pin uses this interface to negotiate allocator requirements and deliver samples to the input pin.

Applications typically do not use this interface.

<b>Filter developers: </b>The <a href="/windows/desktop/DirectShow/cbaseinputpin">CBaseInputPin</a> class implements this interface.

## -inheritance

The <b>IMemInputPin</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMemInputPin</b> also has these types of members:

