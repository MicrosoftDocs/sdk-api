---
UID: NF:upnphost.IUPnPDeviceProvider.Start
title: IUPnPDeviceProvider::Start
author: windows-sdk-content
description: The Start method starts the device provider. The device host invokes this method after it loads the device provider This method performs any initialization required by the device provider.
old-location: upnp\iupnpdeviceprovider_start.htm
tech.root: UPnP
ms.assetid: a76c7063-bad5-4f59-a5ca-8a8a4a79787e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IUPnPDeviceProvider interface [UPnP APIs],Start method, IUPnPDeviceProvider.Start, IUPnPDeviceProvider::Start, Start, Start method [UPnP APIs], Start method [UPnP APIs],IUPnPDeviceProvider interface, _upnp_iupnpdeviceprovider_start, upnp.iupnpdeviceprovider_start, upnphost/IUPnPDeviceProvider::Start
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
 - IUPnPDeviceProvider.Start
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPDeviceProvider::Start


## -description


The 
<b>Start</b> method starts the device provider. The device host invokes this method after it loads the device provider This method performs any initialization required by the device provider.


## -parameters




### -param bstrInitString [in]

Identifies the initialization string specific to a device provider. This string is the same as the one passed to 
<a href="https://msdn.microsoft.com/40f91b29-b535-46e7-834f-97f1a46084f7">IUPnPRegistrar::RegisterDeviceProvider</a> at registration.


## -returns



When implementing this method, return S_OK if the method succeeds. Otherwise, return one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/daaa8b55-bcef-4142-8f7b-e6f64e0ac258">IUPnPDeviceProvider</a>



<a href="https://msdn.microsoft.com/c8e4cd95-a6dc-4bf9-921e-63fbac743028">IUPnPDeviceProvider::Stop</a>
 

 

