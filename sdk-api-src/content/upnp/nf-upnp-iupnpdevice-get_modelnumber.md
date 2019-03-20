---
UID: NF:upnp.IUPnPDevice.get_ModelNumber
title: IUPnPDevice::get_ModelNumber (upnp.h)
author: windows-sdk-content
description: The ModelNumber property specifies a human-readable form of the model number of the device.
old-location: upnp\iupnpdevice_modelnumber.htm
tech.root: upnp
ms.assetid: 7e9b92a6-efad-41f0-b083-a2fed0f70c8b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_ModelNumber method, IUPnPDevice.get_ModelNumber, IUPnPDevice::get_ModelNumber, _upnp_iupnpdevice_modelnumber, get_ModelNumber, get_ModelNumber method [UPnP APIs], get_ModelNumber method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_modelnumber, upnp/IUPnPDevice::get_ModelNumber
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDevice.get_ModelNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPDevice::get_ModelNumber


## -description


The 
<b>ModelNumber</b> property specifies a human-readable form of the model number of the device.


## -parameters




### -param pbstr [out]

Receives a reference to a string that contains the model number. Release this string with <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> when it is no longer required. If the device does not specify a model number, this parameter is set to <b>NULL</b>.


## -returns



For C++: If this property's "get" method succeeds, the return value is S_OK. If the device does not specify a model number, the return value is S_FALSE and <i>pbstr</i> is <b>NULL</b>. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



This property is optional and <i>pbstr</i> can return <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a>



<a href="https://msdn.microsoft.com/c71868ab-e05d-4e6a-b157-4474afc8f61f">IUPnPDevice::ModelName</a>



<a href="https://msdn.microsoft.com/e9f3231a-5836-4629-9df5-6ed9184fb753">IUPnPDevice::ModelURL</a>
 

 

