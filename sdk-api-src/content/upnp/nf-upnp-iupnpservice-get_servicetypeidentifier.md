---
UID: NF:upnp.IUPnPService.get_ServiceTypeIdentifier
title: IUPnPService::get_ServiceTypeIdentifier
author: windows-sdk-content
description: The ServiceTypeIdentifier property specifies the service type identifier for the device.
old-location: upnp\iupnpservice_servicetypeidentifier.htm
old-project: UPnP
ms.assetid: 440344c9-b229-421b-b8a7-76f2f98c2c6b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUPnPService interface [UPnP APIs],get_ServiceTypeIdentifier method, IUPnPService.get_ServiceTypeIdentifier, IUPnPService::get_ServiceTypeIdentifier, _upnp_iupnpservice_servicetypeidentifier, get_ServiceTypeIdentifier, get_ServiceTypeIdentifier method [UPnP APIs], get_ServiceTypeIdentifier method [UPnP APIs],IUPnPService interface, upnp.iupnpservice_servicetypeidentifier, upnp/IUPnPService::get_ServiceTypeIdentifier
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
 - IUPnPService.get_ServiceTypeIdentifier
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPService::get_ServiceTypeIdentifier


## -description


The 
<b>ServiceTypeIdentifier</b> property specifies the service type identifier for the device.


## -parameters




### -param pVal [out]

Receives a reference to a string that contains the service type identifier. Release this string with <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> when it is no longer required.


## -returns



For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/48b20b03-62a4-4dcd-8eda-f1bfef1eef38">IUPnPService</a>
 

 

