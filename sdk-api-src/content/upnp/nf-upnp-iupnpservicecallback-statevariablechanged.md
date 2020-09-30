---
UID: NF:upnp.IUPnPServiceCallback.StateVariableChanged
title: IUPnPServiceCallback::StateVariableChanged (upnp.h)
description: The StateVariableChanged method is invoked when a state variable has changed.
helpviewer_keywords: ["IUPnPServiceCallback interface [UPnP APIs]","StateVariableChanged method","IUPnPServiceCallback.StateVariableChanged","IUPnPServiceCallback::StateVariableChanged","StateVariableChanged","StateVariableChanged method [UPnP APIs]","StateVariableChanged method [UPnP APIs]","IUPnPServiceCallback interface","_upnp_iupnpservicecallback_statevariablechanged","upnp.iupnpservicecallback_statevariablechanged","upnp/IUPnPServiceCallback::StateVariableChanged"]
old-location: upnp\iupnpservicecallback_statevariablechanged.htm
tech.root: upnp
ms.assetid: 68dac38e-535b-491e-a9a5-0f6bccb7fcc1
ms.date: 12/05/2018
ms.keywords: IUPnPServiceCallback interface [UPnP APIs],StateVariableChanged method, IUPnPServiceCallback.StateVariableChanged, IUPnPServiceCallback::StateVariableChanged, StateVariableChanged, StateVariableChanged method [UPnP APIs], StateVariableChanged method [UPnP APIs],IUPnPServiceCallback interface, _upnp_iupnpservicecallback_statevariablechanged, upnp.iupnpservicecallback_statevariablechanged, upnp/IUPnPServiceCallback::StateVariableChanged
req.header: upnp.h
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
req.dll: Upnp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPServiceCallback::StateVariableChanged
 - upnp/IUPnPServiceCallback::StateVariableChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPServiceCallback.StateVariableChanged
---

# IUPnPServiceCallback::StateVariableChanged


## -description

The 
<b>StateVariableChanged</b> method is invoked when a state variable has changed.

## -parameters

### -param pus [in]

Reference to an 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpservice">IUPnPService</a> object that specifies the service about which the UPnP framework is sending the notification.

### -param pcwszStateVarName [in]

Reference to a string that specifies the name of the state variable that has changed.

### -param vaValue [in]

Specifies the new value. The type of the data returned depends on the data type of the state variable for which the notification is sent.

## -returns

The application should return S_OK.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpservice">IUPnPService</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpservice-addcallback">IUPnPService::AddCallback</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpservicecallback">IUPnPServiceCallback</a>