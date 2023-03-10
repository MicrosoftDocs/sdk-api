---
UID: NN:control.IMediaEvent
title: IMediaEvent (control.h)
description: The IMediaEvent interface contains methods for retrieving event notifications and for overriding the Filter Graph Manager's default handling of events.
helpviewer_keywords: ["IMediaEvent","IMediaEvent interface [DirectShow]","IMediaEvent interface [DirectShow]","described","IMediaEventInterface","control/IMediaEvent","dshow.imediaevent"]
old-location: dshow\imediaevent.htm
tech.root: dshow
ms.assetid: 651561d1-4e7e-48de-9cba-769ddb553e63
ms.date: 12/05/2018
ms.keywords: IMediaEvent, IMediaEvent interface [DirectShow], IMediaEvent interface [DirectShow],described, IMediaEventInterface, control/IMediaEvent, dshow.imediaevent
req.header: control.h
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
 - IMediaEvent
 - control/IMediaEvent
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
 - IMediaEvent
---

# IMediaEvent interface


## -description

The <code>IMediaEvent</code> interface contains methods for retrieving event notifications and for overriding the Filter Graph Manager's default handling of events. The <a href="/windows/desktop/api/control/nn-control-imediaeventex">IMediaEventEx</a> interface inherits this interface and extends it.

The Filter Graph Manager implements this interface. Applications can use it to respond to events that occur in the filter graph, such as the end of a stream or a rendering error. Filters post events to the filter graph using the <a href="/windows/desktop/api/strmif/nn-strmif-imediaeventsink">IMediaEventSink</a> interface.

For more information about event notification, see <a href="/windows/desktop/DirectShow/event-notification-in-directshow">Event Notification in DirectShow</a>. For a list of system-defined event notifications, see <a href="/windows/desktop/DirectShow/event-notification-codes">Event Notification Codes</a>.

## -inheritance

The <b>IMediaEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMediaEvent</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
