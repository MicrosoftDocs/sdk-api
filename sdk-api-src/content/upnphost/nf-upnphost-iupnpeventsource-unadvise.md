---
UID: NF:upnphost.IUPnPEventSource.Unadvise
title: IUPnPEventSource::Unadvise (upnphost.h)
description: The Unadvise method is invoked by the device host to stop receiving events. The device host passes in the same pointer that it did when it invoked the IUPnPEventSource::Advise method.
helpviewer_keywords: ["IUPnPEventSource interface [UPnP APIs]","Unadvise method","IUPnPEventSource.Unadvise","IUPnPEventSource::Unadvise","Unadvise","Unadvise method [UPnP APIs]","Unadvise method [UPnP APIs]","IUPnPEventSource interface","_upnp_iupnpeventsource_unadvise","upnp.iupnpeventsource_unadvise","upnphost/IUPnPEventSource::Unadvise"]
old-location: upnp\iupnpeventsource_unadvise.htm
tech.root: upnp
ms.assetid: 6ae9c53f-eb82-4396-ba85-c95e252911c8
ms.date: 12/05/2018
ms.keywords: IUPnPEventSource interface [UPnP APIs],Unadvise method, IUPnPEventSource.Unadvise, IUPnPEventSource::Unadvise, Unadvise, Unadvise method [UPnP APIs], Unadvise method [UPnP APIs],IUPnPEventSource interface, _upnp_iupnpeventsource_unadvise, upnp.iupnpeventsource_unadvise, upnphost/IUPnPEventSource::Unadvise
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
 - IUPnPEventSource::Unadvise
 - upnphost/IUPnPEventSource::Unadvise
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
 - IUPnPEventSource.Unadvise
---

# IUPnPEventSource::Unadvise


## -description

The 
<b>Unadvise</b> method is invoked by the device host to stop receiving events. The device host passes in the same pointer that it did when it invoked the 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpeventsource-advise">IUPnPEventSource::Advise</a> method.

After this method is invoked, the hosted service releases the reference to the event sink that it held.

## -parameters

### -param pesSubscriber [in]

Pointer to the device host's 
<a href="/windows/desktop/api/upnphost/nn-upnphost-iupnpeventsink">IUPnPEventSink</a> interface. This must be the same pointer that was passed when 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpeventsource-advise">IUPnPEventSource::Advise</a> was invoked.

## -returns

When implementing this method, return S_OK if the method succeeds. Otherwise, return one of the COM error codes defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/upnphost/nn-upnphost-iupnpeventsource">IUPnPEventSource</a>



<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpeventsource-advise">IUPnPEventSource::Advise</a>