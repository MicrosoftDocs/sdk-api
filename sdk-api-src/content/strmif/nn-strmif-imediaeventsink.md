---
UID: NN:strmif.IMediaEventSink
title: IMediaEventSink (strmif.h)
description: Notifies the Filter Graph Manager of events that occur within the filter graph.
helpviewer_keywords: ["IMediaEventSink","IMediaEventSink interface [DirectShow]","IMediaEventSink interface [DirectShow]","described","IMediaEventSinkInterface","dshow.imediaeventsink","strmif/IMediaEventSink"]
old-location: dshow\imediaeventsink.htm
tech.root: dshow
ms.assetid: 50aa04b4-9a04-4d0d-a558-42595a69aef7
ms.date: 12/05/2018
ms.keywords: IMediaEventSink, IMediaEventSink interface [DirectShow], IMediaEventSink interface [DirectShow],described, IMediaEventSinkInterface, dshow.imediaeventsink, strmif/IMediaEventSink
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
 - IMediaEventSink
 - strmif/IMediaEventSink
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
 - IMediaEventSink
---

# IMediaEventSink interface


## -description

Notifies the Filter Graph Manager of events that occur within the filter graph. Filters use this interface to report events. The Filter Graph Manager exposes this interface.

Applications do not use <code>IMediaEventSink</code>. To retrieve events, applications use the <a href="/windows/desktop/api/control/nn-control-imediaeventex">IMediaEventEx</a> interface.

## -inheritance

The <b>IMediaEventSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMediaEventSink</b> also has these types of members:

