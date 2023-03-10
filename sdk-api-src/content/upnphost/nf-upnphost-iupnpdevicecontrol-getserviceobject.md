---
UID: NF:upnphost.IUPnPDeviceControl.GetServiceObject
title: IUPnPDeviceControl::GetServiceObject (upnphost.h)
description: The GetServiceObject method is used to obtain the IDispatch pointer to a specific service object. The device host invokes this method once per service, the first time it receives a request for a service.
helpviewer_keywords: ["GetServiceObject","GetServiceObject method [UPnP APIs]","GetServiceObject method [UPnP APIs]","IUPnPDeviceControl interface","IUPnPDeviceControl interface [UPnP APIs]","GetServiceObject method","IUPnPDeviceControl.GetServiceObject","IUPnPDeviceControl::GetServiceObject","_upnp_iupnpdevicecontrol_getserviceobject","upnp.iupnpdevicecontrol_getserviceobject","upnphost/IUPnPDeviceControl::GetServiceObject"]
old-location: upnp\iupnpdevicecontrol_getserviceobject.htm
tech.root: upnp
ms.assetid: 55b54edf-fd1d-45b8-95d4-a746a60e5310
ms.date: 12/05/2018
ms.keywords: GetServiceObject, GetServiceObject method [UPnP APIs], GetServiceObject method [UPnP APIs],IUPnPDeviceControl interface, IUPnPDeviceControl interface [UPnP APIs],GetServiceObject method, IUPnPDeviceControl.GetServiceObject, IUPnPDeviceControl::GetServiceObject, _upnp_iupnpdevicecontrol_getserviceobject, upnp.iupnpdevicecontrol_getserviceobject, upnphost/IUPnPDeviceControl::GetServiceObject
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
 - IUPnPDeviceControl::GetServiceObject
 - upnphost/IUPnPDeviceControl::GetServiceObject
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
 - IUPnPDeviceControl.GetServiceObject
---

# IUPnPDeviceControl::GetServiceObject


## -description

The 
<b>GetServiceObject</b> method is used to obtain the <b>IDispatch</b> pointer to a specific service object. The device host invokes this method once per service, the first time it receives a request for a service.

## -parameters

### -param bstrUDN [in]

Specifies the UDN of the device.

### -param bstrServiceId [in]

Specifies the Service ID of the service for which to obtain the pointer.

### -param ppdispService [out]

Receives the <b>IDispatch</b> pointer to the service object.

## -returns

When implementing this method, return S_OK if the method succeeds. Otherwise, return one of the COM error codes defined in WinError.h.

## -remarks

This method is invoked by the device host when a control request or event subscription is received for a particular service.

Embedded devices are differentiated by their UDNs.

## -see-also

<a href="/windows/desktop/api/upnphost/nn-upnphost-iupnpdevicecontrol">IUPnPDeviceControl</a>



<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpdevicecontrol-initialize">Initialize</a>