---
UID: NF:upnp.IUPnPService.AddCallback
title: IUPnPService::AddCallback (upnp.h)
description: The AddCallback method registers an application's callback with the UPnP framework.
helpviewer_keywords: ["AddCallback","AddCallback method [UPnP APIs]","AddCallback method [UPnP APIs]","IUPnPService interface","IUPnPService interface [UPnP APIs]","AddCallback method","IUPnPService.AddCallback","IUPnPService::AddCallback","_upnp_iupnpservice_addcallback","upnp.iupnpservice_addcallback","upnp/IUPnPService::AddCallback"]
old-location: upnp\iupnpservice_addcallback.htm
tech.root: upnp
ms.assetid: f5797907-ae65-48e6-adf8-b717bfb5101f
ms.date: 12/05/2018
ms.keywords: AddCallback, AddCallback method [UPnP APIs], AddCallback method [UPnP APIs],IUPnPService interface, IUPnPService interface [UPnP APIs],AddCallback method, IUPnPService.AddCallback, IUPnPService::AddCallback, _upnp_iupnpservice_addcallback, upnp.iupnpservice_addcallback, upnp/IUPnPService::AddCallback
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
 - IUPnPService::AddCallback
 - upnp/IUPnPService::AddCallback
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
 - IUPnPService.AddCallback
---

# IUPnPService::AddCallback


## -description

The 
<b>AddCallback</b> method registers an application's callback with the UPnP framework.

## -parameters

### -param pUnkCallback [in]

Specifies the reference to the interface that contains the callback to register. The object referred to by <i>pUnkCallback</i> must either support the 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpservicecallback">IUPnPServiceCallback</a> interface or the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

Do not call this method from within a callback; memory corruption occurs.

If more than one callback is registered, the UPnP framework invokes the callbacks sequentially.

The object referred to by <i>pUnkCallback</i> must either support the 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpservicecallback">IUPnPServiceCallback</a> interface or the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. The 
<b>AddCallback</b> method first queries <i>pUnkCallback</i> for the 
<b>IUPnPServiceCallback</b> interface. If this interface is not supported, the 
<b>AddCallback</b> method then queries <i>pUnkCallback</i> for the <b>IDispatch</b> interface. If the <b>IDispatch</b> interface is not supported, both checks have failed and the 
<b>AddCallback</b> method returns E_FAIL.

If only <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> is supported, the <a href="/windows/desktop/UPnP/s-gly">service object</a> invokes the callback by calling <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">IDispatch::Invoke</a> with the dispatch ID specified as zero, which indicates the default method. This default <b>IDispatch</b> method is passed the same parameters as the 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpservicecallback">IUPnPServiceCallback</a> method, but the first parameter passed is a string that indicates the reason the callback is invoked. Valid values are VARIABLE_UPDATE and SERVICE_INSTANCE_DIED.


This method has the following arguments:

<ul>
<li>The reason the callback is invoked. It is invoked either because a state variable changed (VARIABLE_UPDATE) or because the service instance has become unavailable (SERVICE_INSTANCE_DIED).</li>
<li>The service object for which the callback is invoked.</li>
</ul>



If the callback is invoked for a state variable change, the method is passed two additional arguments:

<ul>
<li>The name of the variable that changed.</li>
<li>The new value.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpservice">IUPnPService</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpservicecallback">IUPnPServiceCallback</a>