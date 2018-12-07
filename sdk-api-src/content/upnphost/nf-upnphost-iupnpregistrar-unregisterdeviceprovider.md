---
UID: NF:upnphost.IUPnPRegistrar.UnregisterDeviceProvider
title: IUPnPRegistrar::UnregisterDeviceProvider
author: windows-sdk-content
description: The UnregisterDeviceProvider method permanently unregisters and unloads the device provider from the device host. The IUPnPDeviceProvider::Stop method is invoked.
old-location: upnp\iupnpregistrar_unregisterdeviceprovider.htm
tech.root: upnp
ms.assetid: 548bd520-9c62-4dae-8ae3-94e3683a34f1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUPnPRegistrar interface [UPnP APIs],UnregisterDeviceProvider method, IUPnPRegistrar.UnregisterDeviceProvider, IUPnPRegistrar::UnregisterDeviceProvider, UnregisterDeviceProvider, UnregisterDeviceProvider method [UPnP APIs], UnregisterDeviceProvider method [UPnP APIs],IUPnPRegistrar interface, _upnp_iupnpregistrar_unregisterdeviceprovider, upnp.iupnpregistrar_unregisterdeviceprovider, upnphost/IUPnPRegistrar::UnregisterDeviceProvider
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# IUPnPRegistrar::UnregisterDeviceProvider


## -description


The 
<b>UnregisterDeviceProvider</b> method permanently unregisters and unloads the device provider from the device host. The 
<a href="https://msdn.microsoft.com/c8e4cd95-a6dc-4bf9-921e-63fbac743028">IUPnPDeviceProvider::Stop</a> method is invoked.


## -parameters




### -param bstrProviderName [in]

Specifies the provider name. Use the same name that was used in the call to 
<a href="https://msdn.microsoft.com/40f91b29-b535-46e7-834f-97f1a46084f7">RegisterDeviceProvider</a>.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/c851e102-4f03-4a21-9e62-9b5c60a728f3">IUPnPRegistrar</a>
 

 

