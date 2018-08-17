---
UID: NF:upnp.IUPnPDevice.get_Services
title: IUPnPDevice::get_Services
author: windows-sdk-content
description: The Services property specifies the list of services provided by the device.
old-location: upnp\iupnpdevice_services.htm
old-project: UPnP
ms.assetid: 3b854a5a-a0a9-4236-83c1-98b3671bfc74
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_Services method, IUPnPDevice.get_Services, IUPnPDevice::get_Services, _upnp_iupnpdevice_services, get_Services, get_Services method [UPnP APIs], get_Services method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_services, upnp/IUPnPDevice::get_Services
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: upnp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDevice.get_Services
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPDevice::get_Services


## -description


The 
<b>Services</b> property specifies the list of services provided by the device.


## -parameters




### -param ppusServices [out]

Receives a reference to an 
<a href="https://msdn.microsoft.com/8d5e487f-d2d4-4603-918c-e751d698be3c">IUPnPServices</a> collection that enumerates the services provided by the device. This reference must be released when it is no longer required.


## -returns



For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a>



<a href="https://msdn.microsoft.com/8d5e487f-d2d4-4603-918c-e751d698be3c">IUPnPServices</a>
 

 

