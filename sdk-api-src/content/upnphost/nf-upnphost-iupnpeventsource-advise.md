---
UID: NF:upnphost.IUPnPEventSource.Advise
title: IUPnPEventSource::Advise (upnphost.h)
description: The Advise method is invoked by the device host to begin receiving events from the hosted service.
helpviewer_keywords: ["Advise","Advise method [UPnP APIs]","Advise method [UPnP APIs]","IUPnPEventSource interface","IUPnPEventSource interface [UPnP APIs]","Advise method","IUPnPEventSource.Advise","IUPnPEventSource::Advise","_upnp_iupnpeventsource_advise","upnp.iupnpeventsource_advise","upnphost/IUPnPEventSource::Advise"]
old-location: upnp\iupnpeventsource_advise.htm
tech.root: upnp
ms.assetid: ec68f4ff-7549-4d48-b347-0320bc55329c
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [UPnP APIs], Advise method [UPnP APIs],IUPnPEventSource interface, IUPnPEventSource interface [UPnP APIs],Advise method, IUPnPEventSource.Advise, IUPnPEventSource::Advise, _upnp_iupnpeventsource_advise, upnp.iupnpeventsource_advise, upnphost/IUPnPEventSource::Advise
req.header: upnphost.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Upnphost.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPEventSource::Advise
 - upnphost/IUPnPEventSource::Advise
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnphost.dll
api_name:
 - IUPnPEventSource.Advise
---

# IUPnPEventSource::Advise


## -description

The 
<b>Advise</b> method is invoked by the device host to begin receiving events from the hosted service. The device host passes a pointer to its <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. The hosted service must query this <b>IUnknown</b> interface for the 
<a href="/windows/desktop/api/upnphost/nn-upnphost-iupnpeventsink">IUPnPEventSink</a> interface the service must use to send event notifications.

## -parameters

### -param pesSubscriber [in]

Pointer to the device host's 
<a href="/windows/desktop/api/upnphost/nn-upnphost-iupnpeventsink">IUPnPEventSink</a> interface.

## -returns

When implementing this method, return S_OK if the method succeeds. Otherwise, return one of the COM error codes defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/upnphost/nn-upnphost-iupnpeventsource">IUPnPEventSource</a>



<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpeventsource-unadvise">IUPnPEventSource::Unadvise</a>