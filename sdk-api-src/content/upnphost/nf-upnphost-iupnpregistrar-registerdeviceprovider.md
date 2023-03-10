---
UID: NF:upnphost.IUPnPRegistrar.RegisterDeviceProvider
title: IUPnPRegistrar::RegisterDeviceProvider (upnphost.h)
description: The RegisterDeviceProvider method registers a device provider with the device host. The device provider is not published on the network. Instead, it creates devices dynamically and registers them using RegisterRunningDevice.
helpviewer_keywords: ["IUPnPRegistrar interface [UPnP APIs]","RegisterDeviceProvider method","IUPnPRegistrar.RegisterDeviceProvider","IUPnPRegistrar::RegisterDeviceProvider","RegisterDeviceProvider","RegisterDeviceProvider method [UPnP APIs]","RegisterDeviceProvider method [UPnP APIs]","IUPnPRegistrar interface","_upnp_iupnpregistrar_registerdeviceprovider","upnp.iupnpregistrar_registerdeviceprovider","upnphost/IUPnPRegistrar::RegisterDeviceProvider"]
old-location: upnp\iupnpregistrar_registerdeviceprovider.htm
tech.root: upnp
ms.assetid: 40f91b29-b535-46e7-834f-97f1a46084f7
ms.date: 12/05/2018
ms.keywords: IUPnPRegistrar interface [UPnP APIs],RegisterDeviceProvider method, IUPnPRegistrar.RegisterDeviceProvider, IUPnPRegistrar::RegisterDeviceProvider, RegisterDeviceProvider, RegisterDeviceProvider method [UPnP APIs], RegisterDeviceProvider method [UPnP APIs],IUPnPRegistrar interface, _upnp_iupnpregistrar_registerdeviceprovider, upnp.iupnpregistrar_registerdeviceprovider, upnphost/IUPnPRegistrar::RegisterDeviceProvider
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
 - IUPnPRegistrar::RegisterDeviceProvider
 - upnphost/IUPnPRegistrar::RegisterDeviceProvider
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
 - IUPnPRegistrar.RegisterDeviceProvider
---

# IUPnPRegistrar::RegisterDeviceProvider


## -description

The 
<b>RegisterDeviceProvider</b> method registers a device provider with the device host. The device provider is not published on the network. Instead, it creates devices dynamically and registers them using 
<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice">RegisterRunningDevice</a>.

## -parameters

### -param bstrProviderName [in]

Specifies the name of the device provider.

### -param bstrProgIDProviderClass [in]

Specifies the ProgID of object that implements the 
<a href="/windows/desktop/api/upnphost/nn-upnphost-iupnpdeviceprovider">IUPnPDeviceProvider</a> interface. This object must already be registered with COM. This object must be an in-process COM server (CLSCTX_INPROC_SERVER) and must be accessible to <a href="/windows/desktop/Services/localservice-account">LocalService</a>.

### -param bstrInitString [in]

Identifies an initialization string specific to a device provider.

### -param bstrContainerId [in]

Specifies a string that identifies the process group in which the device provider belongs. All devices and device providers with the same container ID are contained in the same process.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

Common errors that can occur when invoking this function include:

<ul>
<li>The necessary COM object was not found.</li>
<li>There is no access to the COM object for <a href="/windows/desktop/Services/localservice-account">LocalService</a>.</li>
<li>Subordinate COM interfaces.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/upnphost/nn-upnphost-iupnpregistrar">IUPnPRegistrar</a>



<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-unregisterdeviceprovider">IUPnPRegistrar::UnregisterDeviceProvider</a>