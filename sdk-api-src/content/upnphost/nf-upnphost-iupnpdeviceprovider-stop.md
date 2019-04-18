---
UID: NF:upnphost.IUPnPDeviceProvider.Stop
title: IUPnPDeviceProvider::Stop (upnphost.h)
author: windows-sdk-content
description: The Stop method stops the device provider.
old-location: upnp\iupnpdeviceprovider_stop.htm
tech.root: upnp
ms.assetid: c8e4cd95-a6dc-4bf9-921e-63fbac743028
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUPnPDeviceProvider interface [UPnP APIs],Stop method, IUPnPDeviceProvider.Stop, IUPnPDeviceProvider::Stop, Stop, Stop method [UPnP APIs], Stop method [UPnP APIs],IUPnPDeviceProvider interface, _upnp_iupnpdeviceprovider_stop, upnp.iupnpdeviceprovider_stop, upnphost/IUPnPDeviceProvider::Stop
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
 - IUPnPDeviceProvider.Stop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPDeviceProvider::Stop


## -description


The 
<b>Stop</b> method stops the device provider. This method is invoked by the device host before it unloads the device provider. This method is invoked when a service stops or the computer is shut down, and performs any cleanup processing required by the device provider.


## -parameters






## -returns



When implementing this method, return S_OK if the method succeeds. Otherwise, return one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/daaa8b55-bcef-4142-8f7b-e6f64e0ac258">IUPnPDeviceProvider</a>



<a href="https://msdn.microsoft.com/a76c7063-bad5-4f59-a5ca-8a8a4a79787e">IUPnPDeviceProvider::Start</a>
 

 

