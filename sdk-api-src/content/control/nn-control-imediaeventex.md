---
UID: NN:control.IMediaEventEx
title: IMediaEventEx (control.h)
description: The IMediaEventEx interface inherits the IMediaEvent interface, which contains methods for retrieving event notifications and for overriding the filter graph's default handling of events.
helpviewer_keywords: ["IMediaEventEx","IMediaEventEx interface [DirectShow]","IMediaEventEx interface [DirectShow]","described","IMediaEventExInterface","control/IMediaEventEx","dshow.imediaeventex"]
old-location: dshow\imediaeventex.htm
tech.root: dshow
ms.assetid: 9d367b0a-c7ec-49d4-a41e-045ac81d2c51
ms.date: 12/05/2018
ms.keywords: IMediaEventEx, IMediaEventEx interface [DirectShow], IMediaEventEx interface [DirectShow],described, IMediaEventExInterface, control/IMediaEventEx, dshow.imediaeventex
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
 - IMediaEventEx
 - control/IMediaEventEx
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
 - IMediaEventEx
---

# IMediaEventEx interface


## -description

The <b>IMediaEventEx</b> interface inherits the <a href="/windows/desktop/api/control/nn-control-imediaevent">IMediaEvent</a> interface, which contains methods for retrieving event notifications and for overriding the filter graph's default handling of events. <b>IMediaEventEx</b> adds methods that enable an application window to receive messages when events occur. 

The Filter Graph Manager implements this interface.

For more information about event notification, see <a href="/windows/desktop/DirectShow/event-notification-in-directshow">Event Notification in DirectShow</a>. For a list of system-defined event notifications, see <a href="/windows/desktop/DirectShow/event-notification-codes">Event Notification Codes</a>.

## -inheritance

The <b>IMediaEventEx</b> interface inherits from <a href="/windows/desktop/api/control/nn-control-imediaevent">IMediaEvent</a>. <b>IMediaEventEx</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/control/nn-control-imediaevent">IMediaEvent</a>
