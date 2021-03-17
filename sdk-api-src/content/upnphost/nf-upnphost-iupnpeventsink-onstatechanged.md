---
UID: NF:upnphost.IUPnPEventSink.OnStateChanged
title: IUPnPEventSink::OnStateChanged (upnphost.h)
description: The OnStateChanged method sends an event to the device host with the list of DISPIDs of the state variables that have changed. The device host must query the service object to obtain the new value for each state variable that has changed.
helpviewer_keywords: ["IUPnPEventSink interface [UPnP APIs]","OnStateChanged method","IUPnPEventSink.OnStateChanged","IUPnPEventSink::OnStateChanged","OnStateChanged","OnStateChanged method [UPnP APIs]","OnStateChanged method [UPnP APIs]","IUPnPEventSink interface","_upnp_iupnpeventsink_onstatechanged","upnp.iupnpeventsink_onstatechanged","upnphost/IUPnPEventSink::OnStateChanged"]
old-location: upnp\iupnpeventsink_onstatechanged.htm
tech.root: upnp
ms.assetid: bb87345e-6a61-48fd-94dc-9a90f756a586
ms.date: 12/05/2018
ms.keywords: IUPnPEventSink interface [UPnP APIs],OnStateChanged method, IUPnPEventSink.OnStateChanged, IUPnPEventSink::OnStateChanged, OnStateChanged, OnStateChanged method [UPnP APIs], OnStateChanged method [UPnP APIs],IUPnPEventSink interface, _upnp_iupnpeventsink_onstatechanged, upnp.iupnpeventsink_onstatechanged, upnphost/IUPnPEventSink::OnStateChanged
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
 - IUPnPEventSink::OnStateChanged
 - upnphost/IUPnPEventSink::OnStateChanged
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
 - IUPnPEventSink.OnStateChanged
---

# IUPnPEventSink::OnStateChanged


## -description

The 
<b>OnStateChanged</b> method sends an event to the device host with the list of DISPIDs of the state variables that have changed. The device host must query the service object to obtain the new value for each state variable that has changed.

This method is unavailable to Visual Basic developers, and those using other languages that do not support native arrays. These developers must use 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpeventsink-onstatechangedsafe">OnStateChangedSafe</a> instead.

## -parameters

### -param cChanges [in]

Specifies the number of variables in <i>rgdispidChanges</i>. The value indicates the number of variables whose values have changed.

### -param rgdispidChanges [in]

Contains a list of the DISPIDs of the state variables that have changed. The number of elements in this buffer is specified by <i>cChanges</i>.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

If <i>cChanges</i> is zero or <i>rgdispidChanges</i> is <b>NULL</b>, E_INVALIDARG is returned.

## -see-also

<a href="/windows/desktop/api/upnphost/nn-upnphost-iupnpeventsink">IUPnPEventSink</a>