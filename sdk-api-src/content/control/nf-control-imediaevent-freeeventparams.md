---
UID: NF:control.IMediaEvent.FreeEventParams
title: IMediaEvent::FreeEventParams (control.h)
description: The FreeEventParams method frees resources associated with the parameters of an event.
helpviewer_keywords: ["FreeEventParams","FreeEventParams method [DirectShow]","FreeEventParams method [DirectShow]","IMediaEvent interface","FreeEventParams method [DirectShow]","IMediaEventEx interface","IMediaEvent interface [DirectShow]","FreeEventParams method","IMediaEvent.FreeEventParams","IMediaEvent::FreeEventParams","IMediaEventEx interface [DirectShow]","FreeEventParams method","IMediaEventEx::FreeEventParams","IMediaEventFreeEventParams","control/IMediaEvent::FreeEventParams","control/IMediaEventEx::FreeEventParams","dshow.imediaevent_freeeventparams"]
old-location: dshow\imediaevent_freeeventparams.htm
tech.root: dshow
ms.assetid: d98f37a4-3482-4cf7-bede-c7e7be70652a
ms.date: 12/05/2018
ms.keywords: FreeEventParams, FreeEventParams method [DirectShow], FreeEventParams method [DirectShow],IMediaEvent interface, FreeEventParams method [DirectShow],IMediaEventEx interface, IMediaEvent interface [DirectShow],FreeEventParams method, IMediaEvent.FreeEventParams, IMediaEvent::FreeEventParams, IMediaEventEx interface [DirectShow],FreeEventParams method, IMediaEventEx::FreeEventParams, IMediaEventFreeEventParams, control/IMediaEvent::FreeEventParams, control/IMediaEventEx::FreeEventParams, dshow.imediaevent_freeeventparams
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
 - IMediaEvent::FreeEventParams
 - control/IMediaEvent::FreeEventParams
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
 - IMediaEvent.FreeEventParams
 - IMediaEventEx.FreeEventParams
---

# IMediaEvent::FreeEventParams


## -description

The <code>FreeEventParams</code> method frees resources associated with the parameters of an event.

## -parameters

### -param lEvCode [in]

Event code.

### -param lParam1 [in]

First event parameter.

### -param lParam2 [in]

Second event parameter.

## -returns

Returns S_OK.

## -remarks

After you call the <a href="/windows/desktop/api/control/nf-control-imediaevent-getevent">IMediaEvent::GetEvent</a> method to retrieve an event notification, you must call <code>FreeEventParams</code>. This method frees any resources that were allocated for the event parameters. Pass in the same variables used for the <b>GetEvent</b> call.


#### Examples


```cpp

hr = pEvent->GetEvent(&evCode, &param1, &param2, 0);
// Handle the event (not shown). 
hr = pEvent->FreeEventParams(evCode, param1, param2);

```

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-imediaevent">IMediaEvent Interface</a>



<a href="/windows/desktop/api/control/nn-control-imediaeventex">IMediaEventEx</a>