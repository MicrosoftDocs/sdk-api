---
UID: NF:upnphost.IUPnPRegistrar.UnregisterDeviceProvider
title: IUPnPRegistrar::UnregisterDeviceProvider (upnphost.h)
author: windows-sdk-content
description: The UnregisterDeviceProvider method permanently unregisters and unloads the device provider from the device host. The IUPnPDeviceProvider::Stop method is invoked.
old-location: upnp\iupnpregistrar_unregisterdeviceprovider.htm
tech.root: upnp
ms.assetid: 548bd520-9c62-4dae-8ae3-94e3683a34f1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUPnPRegistrar interface [UPnP APIs],UnregisterDeviceProvider method, IUPnPRegistrar.UnregisterDeviceProvider, IUPnPRegistrar::UnregisterDeviceProvider, UnregisterDeviceProvider, UnregisterDeviceProvider method [UPnP APIs], UnregisterDeviceProvider method [UPnP APIs],IUPnPRegistrar interface, _upnp_iupnpregistrar_unregisterdeviceprovider, upnp.iupnpregistrar_unregisterdeviceprovider, upnphost/IUPnPRegistrar::UnregisterDeviceProvider
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnphost.dll
api_name:
 - IUPnPRegistrar.UnregisterDeviceProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPRegistrar::UnregisterDeviceProvider


## -description


The 
<b>UnregisterDeviceProvider</b> method permanently unregisters and unloads the device provider from the device host. The 
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpdeviceprovider-stop">IUPnPDeviceProvider::Stop</a> method is invoked.


## -parameters




### -param bstrProviderName [in]

Specifies the provider name. Use the same name that was used in the call to 
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider">RegisterDeviceProvider</a>.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nn-upnphost-iupnpregistrar">IUPnPRegistrar</a>
 

 

