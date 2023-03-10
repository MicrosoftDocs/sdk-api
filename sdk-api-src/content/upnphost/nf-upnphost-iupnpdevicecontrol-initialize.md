---
UID: NF:upnphost.IUPnPDeviceControl.Initialize
title: IUPnPDeviceControl::Initialize (upnphost.h)
description: The Initialize method is used to initialize the device. The device host invokes this method.
helpviewer_keywords: ["IUPnPDeviceControl interface [UPnP APIs]","Initialize method","IUPnPDeviceControl.Initialize","IUPnPDeviceControl::Initialize","Initialize","Initialize method [UPnP APIs]","Initialize method [UPnP APIs]","IUPnPDeviceControl interface","_upnp_iupnpdevicecontrol_initialize","upnp.iupnpdevicecontrol_initialize","upnphost/IUPnPDeviceControl::Initialize"]
old-location: upnp\iupnpdevicecontrol_initialize.htm
tech.root: upnp
ms.assetid: 0c1ea343-f04b-414d-92cf-044cb117bc9c
ms.date: 12/05/2018
ms.keywords: IUPnPDeviceControl interface [UPnP APIs],Initialize method, IUPnPDeviceControl.Initialize, IUPnPDeviceControl::Initialize, Initialize, Initialize method [UPnP APIs], Initialize method [UPnP APIs],IUPnPDeviceControl interface, _upnp_iupnpdevicecontrol_initialize, upnp.iupnpdevicecontrol_initialize, upnphost/IUPnPDeviceControl::Initialize
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
 - IUPnPDeviceControl::Initialize
 - upnphost/IUPnPDeviceControl::Initialize
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
 - IUPnPDeviceControl.Initialize
---

# IUPnPDeviceControl::Initialize


## -description

The 
<b>Initialize</b> method is used to initialize the device. The device host invokes this method.

## -parameters

### -param bstrXMLDesc [in]

Specifies the full XML device description, as published by the device host. The device description is based on the template provided by the device.

### -param bstrDeviceIdentifier [in]

Identifies the device to initialize. This is the same identifier returned by 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-registerdevice">IUPnPRegistrar::RegisterDevice</a> or 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice">IUPnPRegistrar::RegisterRunningDevice</a>. It is also used to retrieve the UDN of the device using 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename">IUPnPRegistrar::GetUniqueDeviceName</a>.

### -param bstrInitString [in]

Specifies the initialization string used when this device was registered.

## -returns

When implementing this method, return S_OK if the method succeeds. Otherwise, return one of the COM error codes defined in WinError.h.

## -remarks

This method is invoked immediately after the device control object is instantiated. It must be invoked before 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject">IUPnPDeviceControl::GetServiceObject</a> is invoked.

The difference between a running device and a non-running device is when the 
<b>Initialize</b> method is invoked.

For running devices, 
<b>Initialize</b> is invoked when 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice">IUPnPRegistrar::RegisterRunningDevice</a> is invoked, and the initialization is completed before <b>IUPnPRegistrar::RegisterRunningDevice</b> returns.

For non-running devices, 
<b>Initialize</b> is not necessarily invoked when 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-registerdevice">IUPnPRegistrar::RegisterDevice</a> is invoked. 
<b>Initialize</b> is invoked when the first control or event request arrives.

The <i>bstrDeviceIdentifier</i> can also be used to call 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename">IUPnPRegistrar::GetUniqueDeviceName</a>.

## -see-also

<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject">GetServiceObject</a>



<a href="/windows/desktop/api/upnphost/nn-upnphost-iupnpdevicecontrol">IUPnPDeviceControl</a>