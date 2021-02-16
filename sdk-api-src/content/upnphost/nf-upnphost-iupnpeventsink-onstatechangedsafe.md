---
UID: NF:upnphost.IUPnPEventSink.OnStateChangedSafe
title: IUPnPEventSink::OnStateChangedSafe (upnphost.h)
description: The OnStateChangedSafe method sends an event to the device host with the list of DISPIDs that have changed. The device host must query the service object to obtain the new value for each state variable that has changed.
helpviewer_keywords: ["IUPnPEventSink interface [UPnP APIs]","OnStateChangedSafe method","IUPnPEventSink.OnStateChangedSafe","IUPnPEventSink::OnStateChangedSafe","OnStateChangedSafe","OnStateChangedSafe method [UPnP APIs]","OnStateChangedSafe method [UPnP APIs]","IUPnPEventSink interface","_upnp_iupnpeventsink_onstatechangedsafe","upnp.iupnpeventsink_onstatechangedsafe","upnphost/IUPnPEventSink::OnStateChangedSafe"]
old-location: upnp\iupnpeventsink_onstatechangedsafe.htm
tech.root: upnp
ms.assetid: 95792229-287c-43f1-b03a-45aa63a9682f
ms.date: 12/05/2018
ms.keywords: IUPnPEventSink interface [UPnP APIs],OnStateChangedSafe method, IUPnPEventSink.OnStateChangedSafe, IUPnPEventSink::OnStateChangedSafe, OnStateChangedSafe, OnStateChangedSafe method [UPnP APIs], OnStateChangedSafe method [UPnP APIs],IUPnPEventSink interface, _upnp_iupnpeventsink_onstatechangedsafe, upnp.iupnpeventsink_onstatechangedsafe, upnphost/IUPnPEventSink::OnStateChangedSafe
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
 - IUPnPEventSink::OnStateChangedSafe
 - upnphost/IUPnPEventSink::OnStateChangedSafe
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
 - IUPnPEventSink.OnStateChangedSafe
---

# IUPnPEventSink::OnStateChangedSafe


## -description

The 
<b>OnStateChangedSafe</b> method sends an event to the device host with the list of DISPIDs that have changed. The device host must query the service object to obtain the new value for each state variable that has changed.

The 
<b>OnStateChangedSafe</b> method can only be used by Visual Basic developers and those using languages that do not support native arrays.

## -parameters

### -param varsadispidChanges [in]

Contains a safearray of the DISPIDs of the state variables that have changed.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/upnphost/nn-upnphost-iupnpeventsink">IUPnPEventSink</a>